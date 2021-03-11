---
date: 2020-03-11
title: Installation Arduino IDE
title_order: 2
categories: arduino
description: Installation of the Arduino IDE
type: Document
set: first-steps-arduino
set_order: 3

resources:
  - name: "Arduino"
    link: https://www.arduino.cc
  - name: "Arduino Old Releases"
    link: https://www.arduino.cc/en/Main/OldSoftwareReleases#previous
image1: /images/2020-03-11-allgemein-arduino-ide-installieren/arduino-download.png
image2: /images/2020-03-11-allgemein-arduino-ide-installieren/arduino-donate.png
---



Before you can program the senseBox using the Arduino IDE, you need to install drivers and software on your computer. 

Look at the manual for your operating system and follow the given steps.

## Download Arduino Software for Windows

> Please use Arduino version 1.8.7 for smooth operation.

The senseBox is a microcontroller with various components and sensors. It is programmed via the development environment _Arduino IDE_. Download version 1.8.7 from the [Arduino Homepage](https://www.arduino.cc/en/Main/OldSoftwareReleases#previous):


{% include image.html image=page.image1 %}

> Please download the zip file and <b> not </b> the Windows Installer to avoid possible problems!

Arduino is an open source project and is financed by donations. Therefore you will be asked for a donation before the download. If you don't want to donate anything you can click on 'JUST DOWNLOAD'.

{% include image.html image=page.image2 %}


Create a new folder on your hard disk and unzip the zip file. The IDE can be started by executing the file 'arduino.exe'.  


## Download Arduino Software for Mac(OSX)

> Please use Arduino version 1.8.7 for smooth operation.

The senseBox is a microcontroller with various components and sensors. It is programmed via the development environment _Arduino IDE_. Download version 1.8.7 from the [Arduino Homepage](https://www.arduino.cc/en/Main/OldSoftwareReleases#previous):

{% include image.html image=page.image1 %}

Arduino is an open source project and is financed by donations. Therefore you will be asked for a donation before the download; you can skip this by clicking on 'JUST DOWNLOAD'.

{% include image.html image=page.image2 %}

An Arduino.app file should appear in your downloads folder. Move this file to your "Applications" folder. By opening the file 'Arduino.app' the IDE can be started. 


## Arduino Software für Linux herunterladen

> Please use Arduino version 1.8.7 for smooth operation.

The senseBox is a microcontroller with various components and sensors. It is programmed via the development environment _Arduino IDE_. Download version 1.8.7 from the [Arduino Homepage](https://www.arduino.cc/en/Main/OldSoftwareReleases#previous):

{% include image.html image=page.image1 %}

Arduino is an open source project and is financed by donations. Therefore you will be asked for a donation before the download; you can skip this by clicking on 'JUST DOWNLOAD'.

{% include image.html image=page.image2 %}

### Installing the IDE on Linux

Linux users can download and unpack the Linux variant. The included 'install.sh' script automatically creates a desktop shortcut. The fastest way to do this is via the terminal. To do this, open the terminal by pressing the keys 'Ctrl + Alt + T' and enter the following commands there:

```text
# if the downloaded file is not stored in the downloads folder, replace "Downloads" with the path to the corresponding folder
cd downloads 
```

```text
# unzip the file with the following command and install Arduino
tar -xvf arduino-1.8.7-linux64.tar.xz
cd arduino-1.8.7
./install.sh
```
To be able to program the Arduino, additional rights are required under Ubuntu 14 & 16. These can be set up for the current user with the following commands \(requires admin rights\):

Run `udevadm monitor --udev` and connect the Arduino via USB to determine the device ID. The specified name at the end of the output \(e.g. `ttyUSB0`\) is the device ID. Terminate `udevadm` with `ctrl+C`, and execute the following commands using the device ID found:

```text
sudo usermod -a -G dialout $(whoami)
sudo chmod a+rw /dev/<device-id>
```

After logging out and logging in again, the Arduino should be programmable from the Arduino IDE!




