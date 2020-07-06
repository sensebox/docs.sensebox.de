---
date: 2020-03-11
title: Temperature and humidity sensor
categories: hardware
description: HDC1080
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.shop/product/temperatur-luftfeuchte
  - name: "TI HDC1080 Datenblatt"
    link: http://www.ti.com/lit/ds/symlink/hdc1080.pdf
image: /images/2020-03-11-sensoren-temperatur-luftfeuchte/sensor_temperatur_luftfeuchte.png
block: /images/2020-03-11-sensoren-temperatur-luftfeuchte/block-temperatur-luftfeuchte-en.svg
---

The HDC1080 is a digital humidity and temperature sensor. The sensor has a high accuracy and a very low power consumption and is therefore ideally suited to the senseBox. The sensors are calibrated ex works and can be used directly. 


{% include image.html image=page.image %}

## Technical Information

* "Plug-in-and-Go" senseBox compatible
* Relative humidity (RH) Operating range 0% to 100%.
* 14 bit measurement resolution
* Relative humidity Accuracy ±4
* Temperature accuracy ±0.2°C
* 2100nA Power supply
* Operating voltage 2.7 V to 5.5 V
* I2C interface


## Programming (Arduino)

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

## Programming (Blockly)

In Blockly the sensor can be read out via the following block:

{% include image.html image=page.block %}

In the block you can choose between the different parameters of the temperature and humidity sensor:

- Temperature in degrees Celsius (°C)
- Air humidity in percent (%)