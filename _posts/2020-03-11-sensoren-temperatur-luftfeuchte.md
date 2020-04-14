---
date: 2020-03-11
title: Temperatur- und Luftfeuchtigkeitssensor
categories: sensoren
description: Temperatur- und Luftfeuchtigkeitssensor (HDC1080)
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.kaufen/product/temperatur-luftfeuchte
  - name: "TI HDC1080 Datenblatt"
    link: http://www.ti.com/lit/ds/symlink/hdc1080.pdf
---

# Temperatur- und Luftfeuchtesensor {#head}
Der HDC1080 ist ein digitaler Feuchtigkeits- und Temperatursensor. Der Sensor hat eine hohe Genauigkeit und eine sehr geringe Stromaufnahme und passt dadurch ideal zur senseBox. Die Sensoren sind ab Werk kalibirert und können direkt eingesetzt werden. 

![Temperatur und Luftfeuchtesensor](https://github.com/sensebox/resources/raw/master/gitbook_pictures/hds%20top.png)

## Technische Information

* "Plug-in-and-Go" senseBox kompatibel
* Relative Luftfeuchte (RH) Betriebsbereich 0% bis 100%
* 14 Bit Messauflösung
* Relative Luftfeuchte Genauigkeit ±4%
* Temperatur Genauigkeit ±0.2°C
* 2100nA Stromzufuhr
* Betriebsspannung 2.7 V bis 5.5 V
* I2C Schnittstelle


## Programmierung

```arduino
#include "SenseBoxMCU.h"
#include <Adafruit_HDC1000.h>
#include <SPI.h>

HDC1080 hdc;

void setup(){
    Serial.begin(9600);
    hdc.begin();
}

void loop(){
    Serial.print("Temperature: ");
    Serial.println(hdc.getTemperature());
    Serial.print("Humidity: ");
    Serial.println(hdc.getHumidity());
}
```