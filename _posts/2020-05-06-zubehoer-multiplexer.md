---
date: 2020-05-06
title:  I2C-Multiplexer
categories: hardware
description: senseBox I2C-Multiplexer
type: Document
resources:
bild: /images/2020-05-06-zubehoer-expander/hub_bottom.png
image1: /images/2020-05-06-zubehoer-expander/datasheet_table.png


---
With a senseBox I2C multiplexer, up to eight devices with the same addressing can be operated in parallel via the I2C bus. This allows, for example, several identical temperature sensors to be connected.

{% include image.html image=page.bild %}

## Technical Information

* "Plug-in-and-Go" senseBox compatible through breakout board with JST connector
* 8x JST connection

## Use
The senseBox I2C multiplexer is based on the [TCA9548A from Texas Instruments](http://www.ti.com/product/TCA9548A), which has already become part of many tutorials from the community. With the following sample code from [Retians Blog](https://arduino-projekte.webnode.at/meine-libraries/i2c-multiplexer-tca9548a/) you can test the multiplex and check which channels something is connected to:

[https://arduino-projekte.webnode.at/_files/200002383-38c7539c19/TCA9548A_Scanner.ino.txt](https://arduino-projekte.webnode.at/_files/200002383-38c7539c19/TCA9548A_Scanner.ino.txt)

For the implementation of the above example we first include the required libraries. `Wire.h` for the I2C functionality and `SenseBoxMCU.h` for the sensor functions. 

```
#include <Wire.h>
#include <SenseBoxMCU.h>
```

Now we define the address of the multiplex and a list of channels to which the sensors are connected. 

```
byte multiplexAddress = 0x77;
byte channels[] = {0,1,2};
```

For the sensor we create an object and start its instance behind the serial connection in the setup function.

```
HDC1080 hdc

void setup() {
    Serial.begin(115200);
    hdc.begin();
}
```

In the loop, the channels are changed continuously with the help of a for loop. For each channel the multiplex is addressed via its address. Then we only pass the number of the channel to which all subsequent commands are sent. This happens until a new channel is communicated. 

```
for (int i = 0; i < (sizeof(channels)/sizeof(channels[0])); i++){
   Wire.beginTransmission(multiplexAddress);
   Wire.write(1 << channels[i]);
   Wire.endTransmission();

   Serial.print(channels[i]);
   Serial.print(F(". channel temperature: "));
   Serial.println(hdc.getTemperature());
}
```

Now the sensors can be read out individually. One can detect minimal deviations among the identical sensors: 

```
0. channel temperature: 21.96
1. channel temperature: 22.09
2. channel temperature: 22.14
```

Equivalently, each I2C device can be used several times with the multiplexer. If more than eight devices with the same identifier are to be operated in parallel, the addressing of the multiplexer can be adapted using the three soldered joints on its back and the following table from its [data sheet](http://www.ti.com/lit/ds/symlink/tca9548a.pdf):

{% include image.html image=page.image1 %}

Highlighted in the table is the default setting with the addressing 0x77.