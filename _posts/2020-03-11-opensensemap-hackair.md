---
date: 2020-03-11
title: hackAIR
categories: opensensemap
description: Instuctions for hackAIR
type: Document
---
It is also possible to send the measured data of the hackAIR home sensors (version 2) to the openSenseMap.

To do this you have to [assemble](http://www.hackair.eu/hackair-home-v2/) your device and transfer the [hackair-v2-advanced](https://github.com/mkraats/hackair-v2-advanced).

Afterwards the openSenseMap configuration is available in the web interface. There you have to register a senseBox with the correct hardware.

## 1. [Registration](https://opensensemap.org/register) of a new senseBox
- Fill in user, location, exposure and name. Group identification could be for example: hackAIR.
- Under the item **"Hardware "** in the step **"my senseBox "** unfold the field **"hackAIR "** and select the appropriate sensor configuration. 
- Complete the registration.
- **Important:** Copy 'SenseBox ID'. This is a 24 characters long string that looks something like this: *58a88c6b650831d8a3625e01
- **Important:** Copy 'access token'. This is a 64 character long string.
- If a correct e-mail address is given, the senseBox ID will be sent again by mail. (for example: *Your senseBox ID is: 58a88c6b650831d8a3625e01*)

## 2. configure hackAIR device
The 'hackAIR home v2' sensor can be easily configured via a website. To do so, connect the device to the power supply.
After that an open network called 'ESP-wemos' should be available. After that you have to do the following steps:

- Use your browser to open the hackAIR home v2 configuration page (http://192.168.4.1).
- Under the item **Configure WiFi** enter the *senseBox-ID* in the field **openSenseMap senseBox ID**.
- Under the item **Configure WiFi** enter the **access token* in the field **senseBox access token
- Click on **Save** at the bottom of the page


