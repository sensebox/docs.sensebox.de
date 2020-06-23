---
date: 2020-03-11
title: Manage boxes
categories: opensensemap
description: Manage senseBoxes
type: Document
resources:
image1: /images/2020-03-11-opensensemap-manage/osem_dashboard-en.png
---

Every registered user can manage any number of boxes on the openSenseMap.
If you want to change the settings of a box afterwards or download the sketch, you can do this via the **Dashboard**.
This is available in the menu bar below the user icon as soon as a user is logged in:

{% include image.html image=page.image1 %}

In the dashboard, you can...

- [register new boxes](/opensensensemap/opensensensemap-register/),
- edit or remove existing boxes,
- download sketches.

## Edit senseBox
By clicking on the *Change* button of a box in the dashboard, any properties of this box can be changed afterwards.
After changes have been made in one of the sections, they will be applied by clicking on the floppy disk icon in the upper right corner.

> ***Note:*** *If the sensor configuration has been changed, the program code of the senseBox must also be updated in most cases. This can be found under the Script tab to copy it into the Arduino IDE. If the WiFi version of the senseBox is used, the SSID and WiFi password in the sketch must be replaced again!

## delete senseBox
If a senseBox is no longer used or the measurements of this box should be removed from the openSenseMap, it can be deleted.
For this purpose, the value 'DELETE' must be entered in the edit mode (see above) in the tab *General* under the field "Delete senseBox".
Then a button appears under the field, by which the senseBox and its measurements are deleted.

> ***Attention:*** *This will irrevocably remove all stored sensor data in addition to the senseBox! Since the measurements can also be valuable for subsequent data evaluation, it must be considered whether the senseBox should be deleted.*
