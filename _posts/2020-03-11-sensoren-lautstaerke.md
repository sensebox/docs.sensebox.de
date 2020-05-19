---
date: 2020-03-11
title: Lautstärkesensor
categories: hardware
description: DFRobot SEN0232 Gravity
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.kaufen/product/lautstarkesensor
  - name: DFRobot SEN0232 Gravity
    link: https://www.mouser.de/pdfdocs/SEN0232_Web.pdf

image1: /images/2020-03-11-sensoren-sound/sound.png   
image2: /images/2020-03-11-sensoren-sound/sound-anschluss.png   
---

Der DFRobot SEN0232 misst die Lautstärke und gibt die Messwerte in Dezibel aus.

{% include image.html image=page.image1 %}

## Technische Informationen

* Maße: 60mm x 43mm x 9mm
* "Plug-in-and-Go" senseBox kompatibel
* Eingangsspannung: 3,3-5V
* Ausgangsspannung: 0,6-2,6V
* Messspanne: zwischen 30dBA und 130 dBA akkurat
* Messintervall: 125ms

{% include image.html image=page.image2 %}


## Programmierung (Arduino)


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



