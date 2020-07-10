---
date: 2020-04-07
title: Sensors
title_order: 2
categories: Blockly
description: First Steps Sensors
type: Document

resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image0: /images/2020-04-08-blockly-sensoren/blockly-sensoren-0-en.svg
image1: /images/2020-04-08-blockly-sensoren/blockly-sensoren-1-en.svg
image2: /images/2020-04-08-blockly-sensoren/blockly-sensoren-2-en.svg
image3: /images/2020-04-08-blockly-sensoren/blockly-sensoren-3-en.svg
image4: /images/2020-04-08-blockly-sensoren/blockly-sensoren-4-en.svg
image5: /images/2020-04-08-blockly-sensoren/blockly-sensoren-5-en.svg
image6: /images/2020-04-08-blockly-sensoren/blockly-sensoren-6-en.svg
image7: /images/2020-04-08-blockly-sensoren/blockly-sensoren-7-en.svg
image8: /images/2020-04-08-blockly-sensoren/blockly-sensoren-8-en.svg
image9: /images/2020-04-08-blockly-sensoren/blockly-sensoren-9-en.svg
image10: /images/2020-04-08-blockly-sensoren/blockly-sensoren-10-en.svg

---

## General
Various environmental sensors are located in the senseBox. In this chapter, we will first restrict ourselves to the sensors already installed on the senseBox MCU or those that can be connected via JST cable. 

> To read out and display measured values, it is best to use the display. In this chapter we use a kind of minimal example to show measured values on the display.

## Accelerometer (BMX055)
The acceleration sensor is already installed on the senseBox MCU. It can give you the acceleration in X-, Y-, and Z-axis and the total acceleration. You can choose the measuring range between 2g, 4g, 8g and 16g.

{% include image.html image=page.image0 %}

> The mean acceleration due to gravity is given in *g* and is rounded off to 9.81 m/s<sup>2</sup>

## Button
A button is already installed on the senseBox MCU. Additional buttons can be connected via the three digital ports. In the dropdown menu different modes for the button can be selected:

- __is pressed__: With this mode you can ask if the block is pressed at the moment. You will get either the value TRUE or FALSE.
- __was pressed__: With this mode you can ask if the block was pressed. Only if the button was pressed and released you will get TRUE back
- __as switch__: If you use this mode you can use the button like a light switch. The status is saved until the button is pressed again


{% include image.html image=page.image10 %}

## Temperature and humidity sensor (HDC1080)
The temperature and humidity sensor is plugged into one of the five I2C/Wire ports. It can give you the temperature in °C and the relative humidity in %.

{% include image.html image=page.image1 %}

## Temperature and Air Pressure Sensor (BMP280)
The temperature and air pressure sensor is plugged into one of the five I2C/Wire ports. It can give you the temperature in °C, the air pressure in Pa and the altitude above sea level in m.

{% include image.html image=page.image2 %}

## Brightness and UV sensor (TSL45315 & VEML6070)
The brightness and UV sensor is connected to one of the five I2C/Wire ports. It can tell you the brightness in lux and the UV intensity in &mu;W/cm<sup>2</sup>.

{% include image.html image=page.image3 %}

## Environmental sensor (BME680)
The environmental sensor is connected to one of the five I2C-Wire ports. It can give you the temperature in °C, relative humidity in %, air pressure in Pa and indoor air quality (IAQ) on a scale of 0-500.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;border-color:#ccc;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:9px 20px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:#ccc;color:#333;background-color:#fff;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:9px 20px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:#ccc;color:#333;background-color:#f0f0f0;}
.tg .tg-ptrm{font-family:"Trebuchet MS", Helvetica, sans-serif !important;;background-color:#ffffff;color:#333333;border-color:#50af47;text-align:center;vertical-align:top}
.tg .tg-w810{font-weight:bold;font-family:"Trebuchet MS", Helvetica, sans-serif !important;;background-color:#ffffff;color:#333333;border-color:#50af47;text-align:right;vertical-align:top}
.tg .tg-61z8{font-weight:bold;font-family:"Trebuchet MS", Helvetica, sans-serif !important;;background-color:#ffffff;color:#333333;border-color:#50af47;text-align:right;vertical-align:middle}
.tg .tg-xdoy{font-family:"Trebuchet MS", Helvetica, sans-serif !important;;background-color:#ffffff;color:#333333;border-color:#50af47;text-align:center;vertical-align:middle}
</style>
<table class="tg">
  <tr>
    <th class="tg-61z8">Value<br></th>
    <th class="tg-xdoy">0-50</th>
    <th class="tg-xdoy">51-100</th>
    <th class="tg-xdoy">101-150</th>
    <th class="tg-xdoy">151-200</th>
    <th class="tg-xdoy">201-250</th>
    <th class="tg-xdoy">251-350</th>
    <th class="tg-xdoy">&gt; 350</th>
  </tr>
  <tr>
    <td class="tg-w810">Air Quality</td>
    <td class="tg-ptrm">Excellent</td>
    <td class="tg-ptrm">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Gut&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</td>
    <td class="tg-ptrm">Lightly<br>polluted</td>
    <td class="tg-ptrm">Moderately<br>polluted</td>
    <td class="tg-ptrm">Heavily<br>polluted</td>
    <td class="tg-ptrm">Severely<br>polluted</td>
    <td class="tg-ptrm">Extremly<br>polluted</td>
  </tr>
</table>
<br>
<br style="clear: both">

{% include image.html image=page.image7 %}

In addition to the parameters mentioned above, the sensor can also give you the calibration value (a status message) and partial quantities CO<sub>2</sub>-equivalent and breathing air VOC of the indoor air quality.

## Fine particular sensor (SDS011)
The fine particular sensor is connected to one of the two UART/Serial ports and the respective port is selected in the block. It can give you the fine dust concentration PM2.5 and PM10 in &mu;g/cm<sup>3</sup>.

{% include image.html image=page.image4 %}

## Soil temperature and soil moisture sensor (SMT50)
The soil temperature and soil moisture sensor is connected to one of the three digital ports and the respective port is selected in the block. It can display the soil temperature in °C and the volumetric water content of the soil in %.

{% include image.html image=page.image5 %}

## GPS module (CAM-M8Q)
The GPS module is connected to one of the five I2C/Wire ports. It can give you latitude, longitude, altitude in meters, current speed, timestamp, time and date.

{% include image.html image=page.image6 %}

## Ultrasonic distance sensor
The ultrasonic distance sensor is connected to one of the three digital ports and the respective port is selected in the block. It can give you the distance in cm.

{% include image.html image=page.image8 %}

## Microphone
The microphone is connected to one of the three digital ports and the respective port is selected in the block. It can give you the volume as a level between 0 and 5V.


{% include image.html image=page.image9 %}

