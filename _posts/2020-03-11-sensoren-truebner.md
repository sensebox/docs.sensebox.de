---
date: 2020-03-11
title: Soil moisture and temperature sensor
categories: hardware
description: Truebner SMT50
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.shop/product/bodenfeuchte-temperatursensor-smt50
  - name: "Truebner SMT50"
    link: http://www.truebner.de/sites/default/files/Anleitung_SMT50_V1.1.pdf
image: /images/2020-03-11-sensoren-truebner/sensoren_bodenfeuchte_temperatur.png
block: /images/2020-03-11-sensoren-truebner/block-bodenfeuchte-temperatur-en.svg
---
The truebner SMT50 is a capacitive soil temperature and humidity sensor and is therefore well suited for various applications in the home garden. Capacitive soil moisture sensors generate an electrical field around their measuring electrodes. The field penetrates into the surrounding soil. The sensor's measuring electronics determine the resulting electrical capacity of the electrodes. The higher the water content in the soil, the greater the measuring capacity of the sensor.

{% include image.html image=page.image %}

## Technical details
- Supply voltage: 3.3 - 30 VDC (direct voltage)
- Current consumption approx. 2.7 mA (measured at 12VDC)
- Measuring range volumetric water content: 0 - 50 % (with +/- 3% accuracy)
- Measuring range temperature: -20 to +85 °C (at +/- 1.0°C accuracy)
- Measurement procedure: FDR (Frequency Domain Response)
- Measuring signal: balanced, bipolar differential

### Dimensions
- Dimensions: approx. 13.5 cm x 2.15 cm
- Weight incl. 10m cable: approx. 235 g


## Programming (Blockly)

In Blockly the sensor can be read out via the following block:

{% include image.html image=page.block %}

In the block you can choose between the different parameters of the soil moisture and temperature sensor:

- Soil temperature in degrees Celsius (°C)
- Soil Moisture