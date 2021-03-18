---
date: 2020-04-07
title: Time
title_order: 11
categories: Blockly
description: First Steps Time
type: Document

resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-04-08-blockly-zeit/blockly-time-1.svg
image2: /images/2020-04-08-blockly-zeit/blockly-time-2.svg
image3: /images/2020-04-08-blockly-zeit/blockly-time-3.svg
image4: /images/2020-04-08-blockly-zeit/blockly-time-4.svg
image5: /images/2020-04-08-blockly-zeit/blockly-time-5.svg
image6: /images/2020-04-08-blockly-zeit/blockly-time-6.svg

---

## Interrupt program code
With the `Wait` blocks you can interrupt your program code for a certain time. During this time the microcontroller pauses and no actions are performed. The time is given in milliseconds (1 second = 1000 milliseconds) or microseconds (1 second = 1000000 microseconds).

{% include image.html image=page.image1 %}
{% include image.html image=page.image2 %}

## Current elapsed time
With the `current elapsed time` blocks, you can display the time that your program code is already running. The runtime is given in milliseconds or microseconds.

{% include image.html image=page.image3 %}
{% include image.html image=page.image4 %}

## Wait forever
With the `Wait forever` block, you can end your program.

{% include image.html image=page.image5 %}

## Measuring interval
With the block `Measuring interval`, you can determine how often your measured values are transmitted. By default (i.e. without measuring interval block) the measured values are transmitted every second.

{% include image.html image=page.image6 %}
