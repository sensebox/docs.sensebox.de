---
date: 2020-04-07
title: Loops
title_order: 8
categories: Blockly
description: Usage of Loops in Blockly
type: Document

image1: /images/2020-04-08-blockly-schleifen/blockly-schleifen-1-en.svg
image2: /images/2020-04-08-blockly-schleifen/blockly-schleifen-2-en.svg
image3: /images/2020-04-08-blockly-schleifen/blockly-schleifen-3-en.svg
---
## General
Loops are among the most important control structures in programming. They help you whenever you want to have one or more statements execute a certain number of repetitions often. There are different types of loops in Blockly, but their functions are always very similar. You can find all loops in the category of the same name in the Toolbox.

## Repeat X times loop
The simplest loop is the 'Repeat X times' loop. In this loop, all commands within the loop are repeated X times.

{% include image.html image=page.image1 %}

## Repeat while loop
The second loop is the 'Repeat until/for' loop. The commands inserted in the loop are only executed if a condition attached in the free block section is true. In the drop-down menu of the blockst you can select whether the commands should be executed **while** a condition applies, or **as long as** a condition applies.

{% include image.html image=page.image2 %}

## Loop with run variable
The third loop is implemented by means of a run variable, which can also be used within the program. First, a variable is initialized with a start value and a maximum value is set for it. Then the run variable is increased by the specified number after each run. Thus, an instruction can be defined for each state of the run variable.

{% include image.html image=page.image3 %}