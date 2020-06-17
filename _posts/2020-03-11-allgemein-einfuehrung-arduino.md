---
date: 2020-03-11
title: Erste Schritte mit der Arduino IDE
title_order: 4
categories: arduino
description: Programmierung der senseBox in der Arduino IDE
type: Document
set: first-steps-arduino
set_order: 5

resources:
image1: /images/2020-03-11-allgemein-einfuehrung-arduino/arduino-buttons-1.png
image2: /images/2020-03-11-allgemein-einfuehrung-arduino/arduino-buttons-2.png
---

Before you can get started, you need to install the Arduino IDE. How this works you can find [here](/general/general-arduino-ide-install//)

## Basics

When you open the IDE, you will immediately see a large white area where you will write your program.
In the black area below you will see status and error messages. It is always worth taking a look at these messages when errors occur.

Finally you should have a look at the small buttons above the white area.

{% include image.html image=page.image1 %}

The checkmark and arrow are the two most important symbols for you:
With the check mark you can have your program checked for typing errors, and with the arrow you transfer your program to the senseBox MCU.

{% include image.html image=page.image2 %}

The other three symbols - starting with the small sheet on the far left - stand for creating a new program, opening a saved one and saving your written program.

## The Arduino sketch
An Arduino program (also known as a "sketch") has a very simple structure consisting of two main components. These two required functions contain blocks of instructions that describe the program flow:

``arduino
void setup(){
    // Statement
}
void loop(){
    // Statement
}
```
The 'setup' function is only executed once when the program is started. In the 'loop' function, however, all statements are repeated in an endless loop. Both functions are mandatory for successfully compiling and executing the program. "Compiling" means translating the program into machine code that can be understood by the Arduino processor; the Arduino IDE does this for us.

A double slash (`//') is used to add comments to the program code. It is always important to comment his program code so that others can understand what happens at a certain point.
