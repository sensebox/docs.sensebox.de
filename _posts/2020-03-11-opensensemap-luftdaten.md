---
date: 2020-03-11
title: luftdaten.info
categories: opensensemap
description: Registering a new luftdaten.info device on the openSenseMap
type: Document
resources:

image1: /images/2020-03-11-opensensemap-luftdaten/01_Sensor_Konfiguration.png
image2: /images/2020-03-11-opensensemap-luftdaten/02_Osem_Konfiguration.png
---

The fine particulate matter sensors of the OK Lab Stuttgart (sensor.community) also allow the measured data to be sent to the openSenseMap. To send the data to the openSenseMap, first of all it must be identified which sensors are used on the particulate matter sensor. This can best be checked in the web interface of the particulate matter sensor.
{% include image.html image=page.image1 %}

Afterwards a "senseBox" must be registered on the openSenseMap with the configuration just received.
If the wrong sensors have been selected during registration, the easiest way is to simply delete the box and register it again with the correct sensor configuration.

## 1. Register a new Device
Create a new senseBox under: [register](https://opensensemap.org/register)
- Fill in user, location, site and name. Group identification could be, for example: Air data.
- Under the item **"Hardware "** in the step **"my senseBox "** unfold the field **"luftdaten.info"** and select the appropriate sensor configuration.
{% include image.html image=page.image2 %}
- Complete registration.
- **Important:** Copy senseBox ID. This is a 24 characters long string that looks something like this: *58a88c6b650831d8a3625e01
- If a correct e-mail address is entered, the senseBox ID will also be sent again by e-mail. (for example: *Your senseBox ID is: 58a88c6b650831d8a3625e01*)


## 2. Configuration of the fine particulate matter sensor
The fine dust sensor from Luftdaten.info can be easily configured via a website. To do this, the IP of the device in the WLAN must first be found out. The best way to do this is to read it off the WLAN router.

- Call up the configuration page of the fine dust sensor with the browser.
- Under the item **More APIs** check the box **Send to openSenseMap**. In the field *senseBox-ID* enter your own senseBox-ID.
- Click on **Save** at the bottom of the page.

