---
date: 2020-03-11
title: Sound level sensor
categories: hardware
description: DFRobot SEN0232 Gravity
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.shop/product/lautstarkesensor
  - name: DFRobot SEN0232 Gravity
    link: https://www.mouser.de/pdfdocs/SEN0232_Web.pdf

image1: /images/2020-03-11-sensoren-sound/sound.png   
image2: /images/2020-03-11-sensoren-sound/sound-anschluss.png   
---

The DFRobot SEN0232 measures the volume and outputs the measured values in decibels.

{% include image.html image=page.image1 %}

## Technical Information

* Dimensions: 60mm x 43mm x 9mm
* "Plug-in-and-Go" senseBox compatible
* Input voltage: 3.3-5V
* Output voltage: 0.6-2.6V
* Measuring span: between 30dBA and 130 dBA accurate
* Measuring interval: 125ms

{% include image.html image=page.image2 %}


## Programming (Arduino)


```arduino
#define SoundSensorPin A1  //this pin read the analog voltage from the sound level meter
#define VREF  5.0  //voltage on AREF pin,default:operating voltage

void setup()
{
    Serial.begin(115200);
}

void loop()
{
    float voltageValue,dbValue;
    voltageValue = analogRead(SoundSensorPin) / 1024.0 * VREF;
    dbValue = voltageValue * 50.0;  //convert voltage to decibel value
    Serial.print(dbValue,1);
    Serial.println(" dBA");
    delay(125);
}
```



