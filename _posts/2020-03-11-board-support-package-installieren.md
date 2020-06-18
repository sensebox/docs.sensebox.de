---
date: 2020-03-11
title: Installation of the Board-Support-Package
title_order: 4
categories: arduino
description: Installation of the senseBoxMCU Board-Support-Package
type: Document
set: first-steps-arduino
set_order: 4
resources:
  - name: "Shop"
    link: https://sensebox.kaufen/product/sensebox-mini
image1: /images/2020-03-11-board-support-package-installieren/Boards-Manager.png
image2: /images/2020-03-11-board-support-package-installieren/Boards-Manager-SAMD.png
image3: /images/2020-03-11-board-support-package-installieren/Boards-Manager-senseBox.png
image4: /images/2020-03-11-board-support-package-installieren/Ardu1.png


---

In order for the Arduino IDE to support your senseBox MCU and you can transfer programs to it, you need to install two board support packages before you start. These contain the necessary drivers and the necessary software to communicate with the processor of the senseBox. The Board Support Package of the senseBox also already contains our senseBox libraries. This provides you with all basic methods for programming the enclosed sensors.

In your Arduino IDE under *Preferences*, add the following URL to the field for *additional board administrator URLs*
```
https://github.com/sensebox/senseBoxMCU-core/raw/master/package_sensebox_index.json
```
<br>
{% include image.html image=page.image4 %}

Then open the *board administrator* under *Tools -> Board:"..." -> Boards Manager* and install the two board support packages called **Arduino SAMD Boards by Arduino** and **senseBox SAMD Boards by senseBox**.

{% include image.html image=page.image1 %}

First type "SAMD" in the search bar at the top and look for the package **Arduino SAMD Boards by Arduino**.

{% include image.html image=page.image2 %}

After you installed the Arduino SAMD package search for **senseBox SAMD Boards by senseBox** and install it.

{% include image.html image=page.image3 %}

>Since we update the **senseBox SAMD Boards** package for you on a regular basis, you should check the board administrator from time to time to see if the **senseBox SAMD Boards** package is still up to date. To do this, open the board administrator as described above and search for **senseBox SAMD Boards**. If you click on the entry in the list, an update button will appear there in case of a new version. Click this to install the latest version. 
