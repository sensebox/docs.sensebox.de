---
date: 2020-04-07
title: LED
title_order: 4
categories: Blockly
description: First Steps LED
type: Document

resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-04-08-blockly-led/blockly-led-1-en.svg
image2: /images/2020-04-08-blockly-led/blockly-led-2-en.svg
image3: /images/2020-04-08-blockly-led/blockly-led-3-en.svg

---

## LED
With the `LED on Digital Pin` block, you can control an LED connected to one of the six digital pins. Select the pin in the __Pin__ drop-down menu and choose whether the LED should be switched 'on' or 'off' in __Status__.

{% include image.html image=page.image1 %}

> BUILTIN_1 and BUILTIN_2 are the fixed LEDs on the senseBox MCU next to the red RESET button.

## RGB LED
With the `RGB LED` block, you can control an RGB LED connected to one of the six digital pins. In the drop-down menu __Pin__ you select the respective pin. Numbers from 0 to 255 can be attached to the __red__, __green__ and __blue__ block sections to determine the intensity of the different color components. A value of 0 means that there is no colour portion, a value of 255 means that the maximum colour portion is present.

{% include image.html image=page.image2 %}

> For example, the colour code for senseBox Green is  
{% include image.html image=page.image3 %}
