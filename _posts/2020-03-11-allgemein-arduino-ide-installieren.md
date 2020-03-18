---
date: 2020-03-11
title: Installation der Arduino IDE
categories: Allgemein
description: Installation der Arduino IDE
type: Document
---


## Arduino IDE installieren

Bevor die senseBox aktiviert werden kann, musst du Treiber sowie eine Software auf deinem Computer installieren. Außerdem ist es vor Inbetriebnahme der senseBox ratsam einen Testlauf durchzuführen, um zu überprüfen, ob die Sensoren korrekt funktionieren und die Kommunikation mit dem Internet reibungslos läuft.

Schau dir die Anleitung für dein Betriebsystem an und folge den angegebenen Schritten.

### Arduino Software für Windows herunterladen

> Bitte benutze Arduino Version 1.8.7 für einen reibungslosen Ablauf.

Die senseBox ist ein Microcontroller mit verschiedenen Komponenten und Sensoren. Sie wird über die Entwicklungsumgebung _Arduino IDE_ programmiert. Lade die Version 1.8.7 von der [Arduino Homepage](https://www.arduino.cc/en/Main/OldSoftwareReleases#previous) herunter:


![ ](https://github.com/sensebox/resources/raw/master/gitbook_pictures/software-install/arduino-view.png)

Arduino ist ein Open-Source Projekt und wird durch Spenden finanziert. Daher wirst du vor dem Download nach einer Spende gefragt; das kannst du überspringen, indem du auf `JUST DOWNLOAD` klickst.

![ ](https://github.com/sensebox/resources/raw/master/gitbook_pictures/software-install/arduino-install-view.png)

<div class="box_warning">
 	<i class="fa fa-exclamation-circle fa-fw" aria-hidden="true" style="color: #f0ad4e"></i>
 	Lade bitte die zip-Datei herunter und <b> nicht </b> den Windows-Installer um mögliche Probleme 
     zu vermeiden!
</div>

Lege auf deiner Festplatte einen neuen Ordner an und entpacke darin die zip-Datei. Durch das Starten der Datei `arduino.exe` kann die IDE gestartet werden.  


### Arduino Software für Mac(OSX) herunterladen

> Bitte benutze Arduino Version 1.8.7 für einen reibungslosen Ablauf.

Die senseBox ist ein Microcontroller mit verschiedenen Komponenten und Sensoren. Sie wird über die Entwicklungsumgebung _Arduino IDE_ programmiert. Lade die Version 1.8.7 von der [Arduino Homepage](https://www.arduino.cc/en/Main/OldSoftwareReleases#previous) herunter:

![ ](https://github.com/sensebox/resources/raw/master/gitbook_pictures/software-install/arduino-view.png)

Arduino ist ein Open-Source Projekt und wird durch Spenden finanziert. Daher wirst du vor dem Download nach einer Spende gefragt; das kannst du überspringen, indem du auf `JUST DOWNLOAD` klickst.

![ ](https://github.com/sensebox/resources/raw/master/gitbook_pictures/software-install/arduino-install-view.png)

In deinem Downloads-Ordner sollte eine Arduino.app-Datei erscheinen. Verschiebe diese Datei in deinen "Programme"-Ordner. Durch Öffnen der Datei `Arduino.app` kann die IDE gestartet werden. 


### Arduino Software für Linux herunterladen

> Bitte benutze Arduino Version 1.8.7 für einen reibungslosen Ablauf.

Die senseBox ist ein Microcontroller mit verschiedenen Komponenten und Sensoren. Sie wird über die Entwicklungsumgebung _Arduino IDE_ programmiert. Lade die Version 1.8.7 von der [Arduino Homepage](https://www.arduino.cc/en/Main/OldSoftwareReleases#previous) herunter:

![ ](https://github.com/sensebox/resources/raw/master/gitbook_pictures/software-install/arduino-view.png)

Arduino ist ein Open-Source Projekt und wird durch Spenden finanziert. Daher wirst du vor dem Download nach einer Spende gefragt; das kannst du überspringen, indem du auf `JUST DOWNLOAD` klickst.

![ ](https://github.com/sensebox/resources/raw/master/gitbook_pictures/software-install/arduino-install-view.png)
### Installation der IDE unter Linux {#installation-der-ide-unter-linux}

Linux-Nutzer können die Linuxvariante herunterladen und entpacken. Das enthaltene `install.sh`-Skript legt automatisch eine Desktopverknüpfung an. Am schnellsten geht dies über das Terminal. Öffne dazu das Terminal, indem du die Tasten `Ctrl + Alt + T` drückst und gib dort die folgenden Befehle ein:

```text
# sollte die heruntergeladene Datei nicht im Downloads-Ordner abgespeichert sein, ersetze "Downloads" durch den Pfad zum entsprechenden Ordner
cd Downloads 
```

```text
# entpacke die Datei mit folgendem Befehl und installiere Arduino
tar -xvf arduino-1.8.7-linux64.tar.xz
cd arduino-1.8.7
./install.sh
```
Um den Arduino programmieren zu können, sind unter Ubuntu 14 & 16 zusätzliche Rechte notwendig. Diese können für den aktuellen Nutzer mit den folgenden Befehlen eingerichtet werden \(benötigt Admin-Rechte\):

Führe `udevadm monitor --udev` aus und schließe den Arduino per USB an, um die Device-ID zu bestimmen. Die angegebene Bezeichnung am Ende der Ausgabe \(zB. `ttyUSB0`\) ist die Device-ID. Beende `udevadm` per `ctrl+C`, und führe noch die folgenden Befehle aus, wobei die herausgefundene Device-ID eingesetzt werden muss:

```text
sudo usermod -a -G dialout $(whoami)
sudo chmod a+rw /dev/<device-id>
```

Nach einem Logout und erneutem Login sollte der Arduino aus der Arduino IDE programmierbar sein!



