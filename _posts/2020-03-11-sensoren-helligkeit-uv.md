---
date: 2020-03-11
title: brightness and UV sensor
categories: hardware
description: TSL45315 and VEML6070
type: Document
resources:
  - name: "Datenblatt"
    link: https://sensebox.kaufen/assets/datenblatt/senseBox-VEML-TSL_v20.pdf
  - name: "Datenblatt Vishay VEML6070"
    link: https://www.vishay.com/docs/84277/veml6070.pdf
image: /images/2020-03-11-sensoren-helligkeit-uv/sensor_helligkeit_uv.png
block: /images/2020-03-11-sensoren-helligkeit-uv/block_helligkeit_uv.svg
---


Two sensors are combined on this senseBox component.

The light intensity is measured with the TSL45315 sensor from AMS-TAOS. This sensor detects the lighting conditions similar to the human eye and outputs the brightness values directly in lux, with a wide dynamic range (3 lux to 220k lux).

The second sensor is a Vishay VEML6070 ultraviolet (UV) light sensor. It converts the intensity of the sun's UV light into digital data. The sensor has excellent UV sensitivity and linearity via Filtron™ technology. It has a good UV radiation measurement even during long solar UV exposure and can compensate excellent temperature fluctuations.

{% include image.html image=page.image %}

## Technical details

### Exposure sensor

* 3.3V - 5V tolerant I2C/TWI interface
* Input voltage range: 3.3V - 5V
* on-board 2.5V voltage regulator
* on-board level converter

### UV sensor

* Operating voltage: 2.7V - 5.5V I2C Interface
* Supports acknowledge function (Active Acknowledge function)
* Temperature compensation: -40°C to +85°C
* Software shutdown control for immunity to flickering fluorescent lamps

### Dimensions
* 25mm x 25mm x 9mm
* Weight: 2.5 g

## Programming (Arduino)

```arduino
#include "SenseBoxMCU.h"
#include <SPI.h>

TSL45315 tsl;
VEML6070 veml;

void setup() {
    Serial.begin(9600);
    tsl.begin();
    veml.begin();
}

void loop() {
    Serial.print("Illuminance: ");
    Serial.println(tsl.getIlluminance());
    Serial.print("UV-Intensity: ");
    Serial.println(veml.getUvIntesity());
}
```

## Programming (Blockly)

In Blockly the sensor can be read out via the following block:

{% include image.html image=page.block %}

In the block you can choose between the different parameters of the brightness/UV sensor:

- Brightness in LUX
- UV exposure in µW/m^2

