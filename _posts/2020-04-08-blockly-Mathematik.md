---
date: 2020-04-07
title: Math
title_order: 9
categories: Blockly
description: First Steps Math
type: Document

resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-04-08-blockly-mathematik/blockly-mathematik-1-en.svg
image2: /images/2020-04-08-blockly-mathematik/blockly-mathematik-2-en.svg
image3: /images/2020-04-08-blockly-mathematik/blockly-mathematik-3-en.svg
image4: /images/2020-04-08-blockly-mathematik/blockly-mathematik-4-en.svg
image5: /images/2020-04-08-blockly-mathematik/blockly-mathematik-5-en.svg
image6: /images/2020-04-08-blockly-mathematik/blockly-mathematik-6-en.svg
image7: /images/2020-04-08-blockly-mathematik/blockly-mathematik-7-en.svg
image8: /images/2020-04-08-blockly-mathematik/blockly-mathematik-8-en.svg
image9: /images/2020-04-08-blockly-mathematik/blockly-mathematik-9-en.svg
image10: /images/2020-04-08-blockly-mathematik/blockly-mathematik-10-en.svg
image11: /images/2020-04-08-blockly-mathematik/blockly-mathematik-11-en.svg
image12: /images/2020-04-08-blockly-mathematik/blockly-mathematik-12-en.svg
image13: /images/2020-04-08-blockly-mathematik/blockly-mathematik-13-en.svg
image14: /images/2020-04-08-blockly-mathematik/blockly-mathematik-14-en.svg
---
## General
In Blockly you have the possibility to perform various mathematical operations. You can calculate numbers, create random numbers and distribute values to another value range.

## Calculating numbers
In Blockly you can perform various mathematical calculations. The following blocks are available:
{% include image.html image=page.image1 %}
{% include image.html image=page.image2 %}
{% include image.html image=page.image3 %}
{% include image.html image=page.image4 %}
{% include image.html image=page.image5 %}
{% include image.html image=page.image6 %}
{% include image.html image=page.image7 %}
{% include image.html image=page.image8 %}
## Random numbers
In Blockly you can get random numbers. There are two different blocks available.

{% include image.html image=page.image11 %}

With the block 'integer random value' you can have an integer random value from a defined value range output. 

{% include image.html image=page.image12 %}

With the block 'Random number (0.0-1.0)` you can output a random decimal number between 0.0 and 1.0.

## Distribute values
With the 'Distribute Value' block you can distribute numbers, e.g. measured values, to a new value range (mapping). This is useful if you want to convert your measured values directly into a percentage between 0 and 100.

{% include image.html image=page.image13 %}

At the free block sections, the limits of the original and the limits of the new value range must be defined using the 'number' blocks.

In the following example, the entire value range of the brightness sensor (from 3 to 200,000 lux) is distributed over a new value range from 0 to 100.

{% include image.html image=page.image14 %}

