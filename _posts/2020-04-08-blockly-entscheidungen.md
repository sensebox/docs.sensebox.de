---
date: 2020-04-07
title: Logic
title_order: 7
categories: Blockly
description: 
type: Document

resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-04-08-blockly-entscheidungen/blockly-logic-1.svg
image2: /images/2020-04-08-blockly-entscheidungen/blockly-logic-2.svg
image3: /images/2020-04-08-blockly-entscheidungen/blockly-logic-3.svg
image4: /images/2020-04-08-blockly-entscheidungen/blockly-logic-4.svg
image5: /images/2020-04-08-blockly-entscheidungen/blockly-logic-5.svg
image6: /images/2020-04-08-blockly-entscheidungen/blockly-logic-6.svg
image7: /images/2020-04-08-blockly-entscheidungen/blockly-logic-7.svg
image8: /images/2020-04-08-blockly-entscheidungen/blockly-logic-8.svg
---

Decisions or branching in programmes are among the most important control structures in programming. They allow you to adapt your program to different conditions.

### If, do relationship
The `if, do` block has two free block sections 'if' and 'do'.

{% include image.html image=page.image1 %}

The actions linked to the free block section 'do' are only executed if the condition linked to the block section 'if' is fulfilled. 

For example, the built-in LED on the senseBox MCU should be switched on *when* the built-in button is pressed.

{% include image.html image=page.image2 %}

Commands added after the 'if, do' block will be executed in any case, even if the condition was not fulfilled before.

### else
With a click on the small cogwheel in the top left corner of the `if, do` block you can add a 'else' block section to the block. Commands stored in this block section will only be executed if the condition **wasn't** fulfilled before. If the condition was filfilled, they are skipped.

For example, here the built-in LED 1 should only light up **when** the built-in button is pressed **else** the built-in LED 2 should be switched on.

{% include image.html image=page.image3 %}

### else if
With a click on the small cogwheel in the top left corner of the `if, do` block, you can add a 'else if' block section to the block. Now first the top 'if' condition is checked, if it is not fulfilled the following 'else if' condition is checked. This way only those commands are executed whose associated condition is true. 

For example, depending on the temperature an LED should be switched on. At temperatures below 0°C LED 1 should be switched on, at exactly 0°C LED 2 and at temperatures above 0°C LED 3.

{% include image.html image=page.image4 %}

## Operators
In Blockly you have the possibility to use different logical operators to compare measured values. With the help of these operators you can also formulate more complex logical expressions by logical operations.

### Logical comparisons
With the block for `logical comparisons` values can be compared. 

{% include image.html image=page.image5 %}


### Logical operations
With the block for 'logical operations' more complex logical Asudrucks can be formulated. For example, a lamp that only lights up when two conditions apply.

{% include image.html image=page.image6 %}

The block offers a choice between the operators 'and' and 'or'.

`and` links two conditions together, so that both must be met for the entire expression to be evaluated as true. 

`Or` combines two conditions so that only one of them must be true for the entire expression to be true.

### not block
With the 'not' block, expressions can be negated. A condition is true if the input value is false and false if it is true.

{% include image.html image=page.image7 %}

### Test block
With the 'test' block, a condition can be checked and actions can be defined which are executed depending on the result.

{% include image.html image=page.image8 %}
