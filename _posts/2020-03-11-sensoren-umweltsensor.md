---
date: 2020-03-11
title: Environmental sensor
categories: hardware
description: BME680
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.shop/product/sensebox-mini
  - name: Bosh BME680
    link: https://www.bosch-sensortec.com/media/boschsensortec/downloads/datasheets/bst-bme680-ds001.pdf
image: /images/2020-03-11-sensoren-umweltsensor/bme.png
block: /images/2020-03-11-sensoren-umweltsensor/block-umweltsensor-en.svg
---
With the BME680 sensor you can measure a variety of phenomena. Air temperature, relative humidity, air pressure and air quality can be determined with the BME680. It is therefore a real all-rounder. 

{% include image.html image=page.image %}

## Technical details
* Fast response time of less than 10 seconds
* "Plug-in-and-Go" senseBox compatible
* deviation for gas measurements of +-15%

## Connection and programming

With the included connection cable you can connect your gas sensor to the "I2C" port of the senseBoxMCU. 
If this is done we can now initialize the sensor in the program code and get the first measured values.

**Attention** The BME gas sensor is not compatible with the BMP280 air pressure sensor. That means you can only connect and read out one of the two at the same time!


## Programming (Blockly)

In Blockly the sensor can be read out via the following block:

{% include image.html image=page.block %}

In the block you can choose between the different parameters of the environmental sensor:

- Temperature in degrees Celsius (°C)
- Air humidity in %
- Air pressure in Pa
- Indoor air quality (IAQ)
- Calibration value
- carbon dioxide equivalent
- Breathing air VOC equivalent

## Calibration value

The status of the calibration can be read off via the IAQ Accuracy value. It is either 0, 1, 2 or 3 and indicates the following:

- IAQ Accuracy = 0 means that the sensor is stabilized (takes about 25 minutes) or that there was a timeout (which should be indicated by a warning/error flag by BSEC ← Must be intercepted in Blockly),
- IAQ Accuracy = 1 means value is not accurate,
- IAQ Accuracy = 2 means sensor is being calibrated,
- IAQ Accuracy = 3 means sensor successfully calibrated.

The IAQ index is therefore only meaningful when IAQ Accuracy = 3. In addition to the value for IAQ, BSEC also provides us with K and VOC equivalent values. 
