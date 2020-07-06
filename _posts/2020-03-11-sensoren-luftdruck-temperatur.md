---
date: 2020-03-11
title: Air pressure and temperature sensor
categories: hardware
description: BMP280
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.shop/product/luftdruck-temperatur
  - name: "Bosch BMP280 Data sheet"
    link: https://www.bosch-sensortec.com/media/boschsensortec/downloads/datasheets/bst-bmp280-ds001.pdf
image: /images/2020-03-11-sensoren-luftdruck-temperatur/bmp_top.png
block: /images/2020-03-11-sensoren-luftdruck-temperatur/block-luftdruck-temperatur-en.svg
---
This sensor measures air pressure and temperature and is based on the Bosch BMP280 sensor.

{% include image.html image=page.image %}


## Technical Information

* "Plug-in-and-Go" senseBox compatible
* Operating pressure 300 to 1100 hPa
* Relative precision ±0.12 hPa
* Absolute precision ±1 hPa
* Operating supply current 2.7μA at 1 Hz sampling frequency
* Dimensions: 25mm x 25mm x 9mm
* Weight: 2.4 g

## Programming (Arduino)

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

## Programming (Blockly)

In Blockly the sensor can be read out via the following block:

{% include image.html image=page.block %}

In the block you can choose between the different parameters of the air pressure/temperature sensor:

- Air pressure in Pascal (Pa)
- Temperature in Celsius (°C)
- Height above sea level in m (a reference air pressure is required)