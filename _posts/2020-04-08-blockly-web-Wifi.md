---
date: 2020-04-07
title: Web - WiFi
title_order: 5
categories: Blockly
description: First Steps WiFi
type: Document

resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-04-08-blockly-web/blockly-Web-Wifi-1-en.svg
image2: /images/2020-04-08-blockly-web/blockly-Web-Wifi-2-en.svg


---
## General
In Blockly you have the different possibilities to realize projects that work with the internet. For all of them you have to connect your senseBox to the internet first.

## WiFi
With the `Connect to WiFi` block you can connect your senseBox to a WiFi network in Setup(). Under SSID you have to enter the network name and under Password the WiFi access password.

{% include image.html image=page.image1 %}
<br>
With the `Initialize WiFi Access Point` block, your senseBox can create a WLAN network that you can join with other devices. In the text field SSID you can set the name of your network.

{% include image.html image=page.image2 %}
