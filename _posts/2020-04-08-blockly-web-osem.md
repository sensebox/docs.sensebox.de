---
date: 2020-04-07
title: Web - openSenseMap
title_order: 5
categories: Blockly
description: First Steps openSenseMap
type: Document

resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de

image3: /images/2020-04-08-blockly-web/blockly-Web-oSeM-1-en.svg
image4: /images/2020-04-08-blockly-web/blockly-Web-oSeM-2-en.svg
---

## openSenseMap
The [openSenseMap](https://www.opensensemap.org) is a free data portal for environmental data. To send data to it you have to create a new senseBox first. After that you will be shown a Box ID and Sensor IDs for each sensor. You can find more information in the openSenseMap section.

To send measured values to the openSenseMap, you must first connect your Box to it. Use the 'Connect to openSenseMap' block to do this. 

{% include image.html image=page.image3 %}
<br>
In the first dropdown menu of the block you can choose whether your senseBox should send to the conventional openSenseMap or to workshop.openSenseMap.

> **opensensensemap.org:** senseBoxes created for long-term measurement series 
> 
> **workshop.opensensemap.org:** senseBoxes created in the course of short experiments or for testing.

In the second dropdown menu of the block you have to select if your senseBox is a stationary or a mobile station and enter the senseBox ID in the text field "senseBox ID" which is displayed after registration.
In the free block section 'sensors' you have to link the connected sensors to the openSenseMap block with the help of the 'Send measured value'.

{% include image.html image=page.image4 %}
<br>
In this block, the sensor ID, which is also displayed after registration, must be added under "Sensor ID" and the respective sensor must be added to the free block section.

> **Attention:** The sensor IDs are sensor specific. It is therefore important to pay attention to which ID is assigned to which sensor/measured value.