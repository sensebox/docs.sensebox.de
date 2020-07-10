---
date: 2020-04-07
title: Text
title_order: 10
categories: Blockly
description: First Steps Text
type: Document

resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-04-08-blockly-text/blockly-text-1.svg
image2: /images/2020-04-08-blockly-text/blockly-text-2-en.svg
image3: /images/2020-04-08-blockly-text/blockly-text-3-en.svg
image4: /images/2020-04-08-blockly-text/blockly-text-4-en.svg
image5: /images/2020-04-08-blockly-text/blockly-text-5-en.svg
image6: /images/2020-04-08-blockly-text/blockly-text-6-en.gif
---

## Text field
With the text field Block `" "` you can create text. Write the desired text in the field between the quotation marks. 

{% include image.html image=page.image1 %}

## Create text with
With the `Create text with` block you can convert measured values into text on the one hand and on the other hand to create compound texts (from several text fields, numbers, measured values or variables). 

{% include image.html image=page.image2 %}

The normal `Create Text with` block can be expanded by clicking on the gear wheel. You can add more elements by clicking and dragging to create text from multiple elements. After editing you can close the window again by clicking on the gear wheel again. 

{% include image.html image=page.image6 %}
## Append text
With the `Append Text` block you can append text to an existing variable.

{% include image.html image=page.image3 %}

## Length of

With the `Length of` block you can get the length of a text block.

{% include image.html image=page.image4 %}

> For example, the text block "senseBox" would be 8 units long.

## is empty?

With the `is empty` block you can check if a given text block is empty (has length 0). The result is either true (if the given text block is actually empty) or false (if there are characters in the text block). 

{% include image.html image=page.image5 %}
