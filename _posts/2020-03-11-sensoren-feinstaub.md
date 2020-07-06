---
date: 2020-03-11
title: Particulate matter sensor
categories: hardware
description: SDS011
type: Document
resources:
  - name: Shop
    link: https://sensebox.kaufen/product/feinstaub-sds011
  - name: Datenblatt NOVA SDS011
    link: https://cdn-reichelt.de/documents/datenblatt/X200/SDS011-DATASHEET.pdf
image: /images/2020-03-11-sensoren-feinstaub/sensoren_feinstaub.png
block: /images/2020-03-11-sensoren-feinstaub/block-feinstaubsensor-en.svg
---

With the SDS011 it is possible to determine the fine dust concentration in the air. The sensor outputs two values: The concentration of PM2.5 (particles < 2.5 um) and PM10 (particles < 10 um). This sensor is equipped with a small fan to suck in air. Inside it there is a laser which, together with a photodiode, measures the number of particles. The results of the measurements are given in µg/m³ (microgram per cubic meter).

{% include image.html image=page.image %}

## Technical details
* "Plug-in-and-Go" senseBox compatible
* Fast response time of less than 10 seconds
* High resolution up to 0.3µg/m3
* Multiple scientific verification of data accuracy

## Programming (Arduino)

```arduino
#include "SenseBoxMCU.h"
#include <SPI.h>
#include <Wire.h>

SDS011 my_sds(Serial1) // Serial1 gibt hier den Seriellen Port an, an dem du den Sensor angeschlossen hast
float p10,p25

```arduino
void setup(){
    // Normalen seriellen Port initialisieren 
    Serial.begin(9600);
    while(!Serial);
    // Seriellen Port an dem unsere Sensor angeschlossen ist initialisieren
    Serial1.begin(9600);
    delay(5000);
}

void loop(){
    // Variablen den gemessenen Feinstaubwerte zuweisen
    p10 = my_sds.getPm10();
    p25 = my_sds.getPm25();
    //Werte in der Konsole drucken
    Serial.println("P2.5: "+String(p25));
    Serial.println("P10:  "+String(p10));
    delay(1000);
}
```

## Programmierung (Blockly)

In Blockly the sensor can be read out via the following block:

{% include image.html image=page.block %}

Select the port to which you have connected the sensor and the measured value via the drop-down menu.

- PM2.5: Fine dust fraction below 2.5 µg/m^3 
- PM10: Fine dust fraction below 10µg/m^3
