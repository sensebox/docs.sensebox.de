---
date: 2020-03-11
title: openRoberta
categories: Blockly
description: Introduction to the Programming interface of openRoberta
type: Document
set: editoren
set_order: 3
resources:
  - name: "openroberta lab"
    link: https://lab.openroberta.org
  - name: "openroberta Wiki"
    link: https://jira.iais.fraunhofer.de/wiki/display/ORInfo  
image1: /images/2020-03-11-allgemein-einfuehrung-openroberta/openroberta-carousel.png
image2: /images/2020-03-11-allgemein-einfuehrung-openroberta/openroberta-oberflaeche-en.png
image3: /images/2020-03-11-allgemein-einfuehrung-openroberta/openroberta-buttons.png

---

openRoberta is a graphical programming interface developed by the Fraunhofer Institute. Besides the senseBox, you can program many other systems via Open Roberta.  

## First Steps
Open the Open Roberta Lab at [lab.open-roberta.org](https://lab.openroberta.org). There you first have to select your system, the senseBox.

{% include image.html image=page.image1 %}

After you have chosen your system, you will find yourself on the programming interface. This can be roughly divided into three areas:
The navigation bar at the top, the toolbox on the left and the large white work area. 

{% include image.html image=page.image2 %}

> By clickling on the Globe Icon in the top right of the navigation bar you can choose your language.

### Navigation bar
The *Navigation bar* can be divided into two areas. In the upper half the buttons "Edit", "Robot", "Help" etc. There, for example, stored programs can be opened or the system can be changed.
In the lower half are the tabs for "Program" and "Robot Configuration". The "Program" tab is open by default and shows you your desktop to write programs. Under the tab "Robot configuration" the different connected sensors and actuators must be specified.

> If a connected component is not specified in the robot configuration, it cannot be used in the program!

### Toolbox
Behind the *Toolbox* are all the blocks you need to program the senseBox. You can simply *drag and drop* into the workspace. All blocks of a category are always colored in the same color as the category.

### Workspace
In the *workspace* you program your senseBox. As you can see, by default there are already two blocks in the 'Start' and 'Repeat infinitely often' workspace. These blocks are essential for every program and therefore cannot be removed.
Furthermore you will find the button in the lower right corner of the workspace to transfer your program to the senseBox, save the program in the cloud, zoom in and out your blocks in the workspace and the trash can to delete blocks.

{% include image.html image=page.image3 %}

## Transferring programs
To transfer your program to the senseBox, you must connect the senseBox to your computer via the USB cable. Next, you can download it by clicking the "Play" button in the lower left corner of the workspace. Now follow the instructions in the Pop-up window.


## openroberta Wiki
This and all other information about the Open Roberta Lab can be found online in the [Documentation on the openroberta-lab from the Fraunhofer Institute] (https://jira.iais.fraunhofer.de/wiki/display/ORInfo ).
