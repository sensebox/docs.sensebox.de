---
date: 2020-04-07
title: LoRa
title_order: 5
categories: Blockly
description: Usage of LoRa blocks in Blockly
type: Document

resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-04-08-blockly-lora/blockly-lora-1-en.svg
image2: /images/2020-04-08-blockly-lora/blockly-lora-2-en.svg
image3: /images/2020-04-08-blockly-lora/blockly-lora-3-en.svg
image4: /images/2020-04-08-blockly-lora/blockly-lora-4-en.svg
image5: /images/2020-04-08-blockly-lora/blockly-lora-5-en.svg
image6: /images/2020-04-08-blockly-lora/blockly-lora-6-en.svg
image7: /images/2020-04-08-blockly-lora/blockly-lora-7-en.svg
image8: /images/2020-04-08-blockly-lora/blockly-lora-8-en.svg
image9: /images/2020-04-08-blockly-lora/blockly-lora-9-en.svg
image10: /images/2020-04-08-blockly-lora/blockly-lora-10-en.svg
image11: /images/2020-04-08-blockly-lora/blockly-lora-11-en.svg
image12: /images/2020-04-08-blockly-lora/blockly-lora-12.svg
image13: /images/2020-04-08-blockly-lora/blockly-lora-13.png
image14: /images/2020-04-08-blockly-lora/blockly-lora-14.png
imageHumidty: /images/2020-04-08-blockly-lora/blockly-lora-humidity-en.svg
imageTemperatur: /images/2020-04-08-blockly-lora/blockly-lora-temperature-en.svg
imageIlluminance: /images/2020-04-08-blockly-lora/blockly-lora-illuminance-en.svg
---
## Activation

{% include image.html image=page.image1 %}

With these blocks you can initialize the Lora-Bee and connect to The Things Network. Depending on which activation method you use (OTAA or ABP) you have to enter the corresponding ID's in the block. Additionally, you can set the transmission interval in minutes.  


## Lora Message
{% include image.html image=page.image2 %}

Use this block to send a message via the LoRa network. No special format is used for the message (often called payload). The data is encoded as bytes so that it can be transmitted quickly and efficiently over the LoRa network. The data must then be converted back into a readable format in the TTN Console using a special decoder. 

## Create Decoder
TTN decoding is all about understanding bytes. Then it is possible to create quick solutions to access your data measured by senseBox.

### Theory
LoRaWAN is not suitable for sending large amounts of data, therefore the information is divided into small bytes and sent. One byte contains 8 bits. This means that you can distinguish between 256 different values. 2 bytes already contain 16 bits, so it is possible to distinguish between 65536 values.

The following table gives an overview of the bandwidth:


| bytes | bit | min (signed) | max (signed) | min (unsigned) | max (unsigned) |
|-------|-----|----------------|---------------|----------------|----------------|
| 1 | 8 | -128 | 127 | 0 | 255 |
| 2 | 16 | −32.768 | 32.767 | 0 | 65.535 |
| 3 | 24 | −2.147.483.648 | 2.147.483.647 | 0 | 4.294.967.295 |

There are two different types in the table: "signed" and "unsigned". Signded values cover both the positive and negative value range. 

Example: You want to measure the humidity. The values are between 0% and 100%. However, they are not decimal numbers but only integer values. You could now use a byte which corresponds to the value for the humidity. However, if you want to send a decimal number with two decimal places, 1 byte is no longer sufficient. 2 bytes must be used.  

Imagine we measure 85.42%. A simple approach would be to take the measurement and multiply it by 100. Now we have a value of 85.42 * 100 = 8542. We can encode 8542 into two bytes, send them to TTN and decode these two bytes to get 8542. This number can now be divided by 100 and we get the value of 85.42%. This is basically how it works.

### Example

__Blockly__:
On the Arduino site the [lora-serialization](https://github.com/thesolarnomad/lora-serialization) library is used. The documentation shows a [function](https://github.com/thesolarnomad/lora-serialization#unsigned-16bit-integer-2-bytes) to send a value with 16 bits. This function can be used to send humidity values. The humidity value is between 0 and 100%, so the following blocks can be used for sending:

{% include image.html image=page.imageHumidty %}

The measured value is multiplied by 100 to maintain the two decimal places. 

As the value for the temperature can also fall into the negative range, the value must first be converted into a positive one and then multiplied by one to retain the two decimal places. 

{% include image.html image=page.imageTemperatur %}

This example uses a temperature sensor that has measured values from -18 degrees Celsius and outputs the temperature with an accuracy of 0.0013 degrees Celsius. 

__TTN__:
In the TTN Console two different values are now coming from the senseBox. These values must now be decoded back from bytes to the original values using a decoder. You can define the decoder under Payloads:

{% include image.html image=page.image13 %}

``js
/**
 * Convert the array of bytes to an unsigned integer, LSB. 
 *
 * BEWARE: This is only safe up to 0x1FFFFFFFFFFF, so: 6 bytes.
 */
function uint(bytes) {

  return bytes.reduceRight(function(acc, b) {
    // We expect an unsigned value, so to support more than 3 bytes
    // don't use any bitwise operators, which would always yield a
    // signed 32 bits integer instead.
    return acc * 0x100 + b;
  }, 0);
}
```

Here you can now define the decoder
```js
function Decoder(bytes) {

  var i = 0;     
  var decoded = {};
  // The index in the bytes array that needs to be handled next;
  // use along with "i++" which returns the current value, and
  // then increments it for the next usage


  // Relative humidity with 0.01 precision, 0.00 through 100.00, LSB
  var humidity = uint(bytes.slice(i, i+=2)) / 100;
  // Temperature with 0.0013 precision, -18.000 through 67.000, LSB
  var temperature = uint(bytes.slice(i, i+=2)) / 771 - 18;
  // Unary plus operator to cast string result of toFixed to number
  temperature = +temperature.toFixed(3);
  
  decoded['TEMPERATURE_SENSOR_ID'] = temperature
  decoded['HUMIDITY_SENSOR_ID'] = humidity
  
  return decoded;
}
```
The function takes the first two bytes and converts them to the humidity reading. The next two bytes are converted to a temperature reading. If you use the openSenseMap as endpoint (`https://ttn.opensensemap.org/v1.1`) in the TTN HTTP integration, the readings are linked to your sensor IDs and the readings are displayed on the openSenseMap. More about the openSenseMap TTN integration can be found [here](https://sensebox.github.io/books-v2/osem/ttn_integration.html)

### Important points
Some important points should be noted:

→ Decoding fails / returns wrong values if you do not send everything that needs to be decoded. For example, if the decoder accepts a humidity and a temperature value, but the senseBox only sends a humidity value, you will not get correct values.

→ When sending values larger than 3 bytes it is a little bit different. Values for brightness can be larger than a 2 byte integer at maximum. Therefore 3 bytes are needed. You can send the whole thing as follows: 

{% include image.html image=page.imageIlluminance%}


and decode as follows:
```js
var lux = bytes[i] | bytes[i+1]<<8 | bytes[i+2]<<16;
i = i + 3 // increment counter afterwards
```

## Cayenne LPP
{% include image.html image=page.image3 %}
The [Cayenne Low Power Payload Format](https://community.mydevices.com/t/cayenne-lpp-2-0/7510) offers an easy way to send data over the LoRaWAN network. The data can be decoded directly into a readable format using an existing decoder. Different blocks are available for different measured values to ensure that all decimal places are transmitted correctly. 

{% include image.html image=page.image5 %}
{% include image.html image=page.image6 %}
{% include image.html image=page.image7 %}
{% include image.html image=page.image8 %}
{% include image.html image=page.image9 %}
{% include image.html image=page.image10 %}
{% include image.html image=page.image11 %}
{% include image.html image=page.image12 %}

In the TTN console you can select the decoder under __Payload__. Select Cayenne LPP and the values will be decoded automatically.

{% include image.html image=page.image14 %}