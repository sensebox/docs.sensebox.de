---
date: 2020-03-11
title: Luftdruck- und Temperatursensor
categories: sensoren
description: Luftdruck- und Temperatursensor (BMP280)
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.kaufen/product/luftdruck-temperatur
  - name: "Bosch BMP280 Data sheet"
    link: https://www.bosch-sensortec.com/media/boschsensortec/downloads/datasheets/bst-bmp280-ds001.pdf
---
Dieser Sensor misst den Luftdruck und die Temperatur und basiert auf dem BMP280 Sensor von Bosch.

![Der Luftdruck- und Temperatursensor](https://github.com/sensebox/resources/raw/master/gitbook_pictures/bmp%20top.png)

## Technische Informationen

* "Plug-in-and-Go" senseBox kompatibel
* Betriebsdruck 300 bis 1100 hPa
* Relative Präzision ±0.12 hPa
* Absolute Präzision ±1 hPa
* Betriebsversorgungsstrom 2.7μA bei 1 Hz Sampling Frequenz
* Maße: 25mm x 25mm x 9mm
* Gewicht: 2,4 g

## Programmierung

```arduino
#include "SenseBoxMCU.h"
#include <SPI.h>

BMP280 bmp_sensor;

void setup() {
  Serial.begin(9600);
  bmp_sensor.begin();
}

void loop() {
    Serial.print("Pressure: ");
    Serial.println(bmp_sensor.getPressure());
    Serial.print("Temperature: ");
    Serial.println(bmp_sensor.getTemperature());
    Serial.print("Altitude: ");
    Serial.println(bmp_sensor.getAltitude(1000));
}
```

## Programmierung (Blockly)

In Blockly kann der Sensor über folgenden Block ausgelesen werden:

![Der Luftdruck- und Temperatursensor](https://github.com/sensebox/resources/raw/master/gitbook_pictures/bmp%20top.png)

Im Block kannst du zwischen Luftdruck und Temperatur auswählen.