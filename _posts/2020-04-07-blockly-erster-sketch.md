---
date: 2020-04-07
title: Your first sketch
title_order: 1 # Indicates the order of apperance on the overview pages
categories: Blockly
description: Write your first program for the senseBox
type: Document
set: blockly-erste-schritte
set_order: 3

resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-04-08-blockly-erste-schritte/blockly-fs-1.svg
image2: /images/2020-04-08-blockly-erste-schritte/blockly-fs-2.svg
image3: /images/2020-04-08-blockly-erste-schritte/blockly-fs-3.svg

---
To get to know Blockly you write a simple program that makes the built-in LED on the senseBox blink.

## Programming

### Step 1: Setup and endless loop

This block is loaded directly when the interface is started and should always be used. The two basic functions `Setup()` and `Loop()` are always needed to write a working program.
All blocks within the `Setup()` function are only executed once at the beginning of the program. In this function for example the display is initialized or the WLAN connection is established. All blocks that are within the `Loop()` function are executed continuously. The microcontroller executes all blocks again and again from top to bottom. In the 'loop()`, for example, the sensors are read out or the measured values are stored on an SD card or transferred to the Internet.

{% include image.html image=page.image1 %}

### Step 2: Switch on the built-in LED

To switch on the built-in LED, you have to pull the 'LED on digital' block into an loop. Then select "BUILTIN_1" under PIN and "On" under Status.

{% include image.html image=page.image2 %}

>The built-in LED can be found above the red reset button on the senseBox MCU.


### Step 3: Let the built-in LED flash

To make the built-in LED flash, it is necessary to switch it off again with another 'LED on digital' block. In addition, a pause must be inserted after switching on and off so that the flashing is visible at all. You can find the 'Waiting' block in the category 'Time'.

{% include image.html image=page.image3 %}

<div class="panel panel-info">
  <div class="panel-heading">
1000 milliseconds are 1 second
  </div>
  <div class="panel-body">
  </div>
</div>