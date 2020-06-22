---
date: 2020-03-11
title: "Step 3: Transfer program code"
title_order: 3
categories: sensebox-home
description: Step 3 for building the senseBox:home
type: Document
set: aufbau-sensebox-home
set_order: 3
image1: /images/sensebox-home/compile-en.png
---

After registration, the program code must be copied to the senseBox. If you have a senseBox with WiFi-Bee or Lan-Bee you can easily compile the program code online and transfer it via drag and drop. You do not need to install any software on your computer

## Compiling online
The easiest way to get your code onto the senseBox is to use our online compiler. You have to enter some information in the mask. If something does not fit your individual structure of the senseBox, you can simply leave this field blank. Finally press "Compile" and a file in the format .BIN will be downloaded by your browser. 

{% include image.html image=page.image1 %}

### Transfering to the senseBox MCU

If you connect your senseBox MCU to your computer and double-click on the red button, it will be recognized as a removable data carrier. With a click on "Compile Code" in the web interface your program code will be compiled on the server and a .BIN file will be offered for download. Depending on which operating system you are using, the copying process differs. 

#### Copying with Windows 

With Windows you can simply drag and drop the created .BIN file to the removable disk <b>SENSEBOX</b>. The red LED on the button will flicker briefly and then the board will restart automatically and execute your program code. 

#### Copying with MacOS

Unfortunately, copying with MacOS by drag & drop does not yet work. One possibility is to copy the file in the terminal using the dd command (only recommended for experienced users!) or to use an alternative file manager such as [muCommander](http://www.mucommander.com/).

#### Copying with Linux 

With Linux you can simply drag and drop the created .BIN file to the removable disk <b>SENSEBOX</b>. The red LED on the button will flicker briefly and then the board will restart automatically and execute your program code. 

<hr>

<a href="/sensebox-home/home-schritt-2/" class="button">Back to step 2</a>