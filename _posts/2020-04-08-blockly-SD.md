---
date: 2020-04-07
title: SD-Card
title_order: 6
categories: Blockly
description: First steps SD-Card
type: Document

resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-04-08-blockly-SD/blockly-SD-1-en.svg
image2: /images/2020-04-08-blockly-SD/blockly-SD-2-en.svg
image3: /images/2020-04-08-blockly-SD/blockly-SD-3-en.svg
image4: /images/2020-04-08-blockly-SD/blockly-SD-4-en.svg

---
With the senseBox, you can use the SD-Bee to save data on a microSD card for later analysis on the computer.

## Store values on SD card
With the `Create File on SD Card` block in Setup() a new file can be created on the SD card. The name of the file can be changed in the block drop down menu.

{% include image.html image=page.image1 %}

With the `Open File on SD Card` block, the previously created file can then be opened in the loop. 

{% include image.html image=page.image2 %}

The `Write data to SD card` block can then be placed in the free block section of the `Open file on SD card` block. The text or number to be written can then be placed in the free block section of the `Write data on SD card` block. In addition, you can determine whether or not a line break should be inserted after each measured value by checking the 'Line break' box. 

{% include image.html image=page.image3 %}

## Example
In the following example, the temperature is stored in a variable and then written to the SD card. More about variables can be found in the chapter with the same name.

{% include image.html image=page.image4 %}
