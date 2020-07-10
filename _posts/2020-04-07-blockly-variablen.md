---
date: 2020-03-11
title: Variables
title_order: 11
categories: Blockly
description: Usage of Variables in Blockly
type: Document

resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-04-08-blockly-variablen/blockly-variables-1.svg
image2: /images/2020-04-08-blockly-variablen/blockly-variables-2.svg
image3: /images/2020-04-08-blockly-variablen/blockly-variables-3.svg
image4: /images/2020-04-08-blockly-variablen/blockly-variables-4.svg
---

## General
Variables are placeholders for numbers, letters and character strings. This means that a variable does not have to remain the same over the entire course of the program. This is especially useful if you want to use a certain information at different places in the program.

Variables can be defined using the 'set item to' block.

{% include image.html image=page.image1 %}

In the drop-down menu of the block, you can rename the variable and create a new variable.

## Example
After a soccer game, you want to store in a variable how many goals were scored. This variable is then shown on the display

{% include image.html image=page.image2 %}

In order to extend the simple example a little, it should now be possible to add points live. For every goal you score, you have to press the built-in button on the MCU once.

{% include image.html image=page.image3 %}

## Data types
Depending on what is stored in a variable you should define the correct data type. You define the data type with the help of the 'as character' block. This block is attached to a 'set item to' block. Afterwards the value to be stored is inserted in the free block section and the data type is selected in the drop down menu.

{% include image.html image=page.image4 %}
<br>

In Blockly there are the following data types:

**Characters:** For single text characters

**Text:** For whole words or sentences

**Boolean:** For values that are either true or false (or 1 or 0)

**Short number:** for single digit numbers

**Number:** For whole numbers from -32,768 to 32,767

**Large number:** For large numbers from -2,147,483,648 to 2,147,483,647

**Decimal:** For decimal numbers    
