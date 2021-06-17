---
date: 2020-03-11
title: Installation der Arduino IDE
title_order: 2
categories: arduino
description: Installation der Arduino IDE
type: Document
set: erste-schritte-arduino
set_order: 3
resources:
  - name: "Arduino"
    link: https://www.arduino.cc
  - name: "Arduino Old Releases"
    link: https://www.arduino.cc/en/Main/OldSoftwareReleases#previous
image1: /images/2020-03-11-allgemein-arduino-ide-installieren/arduino-download.png
image2: /images/2020-03-11-allgemein-arduino-ide-installieren/arduino-donate.png
---



Bevor du die senseBox über die Arduino IDE programmieren kannst, musst du Treiber sowie eine Software auf deinem Computer installieren. 

Schau dir die Anleitung für dein Betriebsystem an und folge den angegebenen Schritten.

## Arduino IDE für Windows herunterladen

Die senseBox besteht aus einem Microcontroller und verschiedenene weitere Komponenten und Sensoren. Der Microcontroller kann über Blockly und openRoberta auch über die Entwicklungsumgebung _Arduino IDE_ programmiert. Lade die aktuellste Version (1.8.15 - Stand Juni 2021) von der [Arduino Homepage](https://www.arduino.cc/en/software) herunter:


{% include image.html image=page.image1 %}

Arduino ist ein Open-Source Projekt und wird durch Spenden finanziert. Daher wirst du vor dem Download nach einer Spende gefragt; falls du nichts spenden möchtest, kannst du auf `JUST DOWNLOAD` klicken.

{% include image.html image=page.image2 %}

Installiere die Arduino IDE und füge im nächsten Schritt das [Board Support Package hinzu](/arduino/board-support-package-installieren/) 


## Arduino IDE für MacOS herunterladen

Die senseBox ist ein Microcontroller mit verschiedenen Komponenten und Sensoren. Sie wird über die Entwicklungsumgebung _Arduino IDE_ programmiert. Lade die Version aktuellste Version (1.8.15 - Stand Juni 2021) von der [Arduino Homepage](https://www.arduino.cc/en/software)  herunter:

{% include image.html image=page.image1 %}

Arduino ist ein Open-Source Projekt und wird durch Spenden finanziert. Daher wirst du vor dem Download nach einer Spende gefragt; das kannst du überspringen, indem du auf `JUST DOWNLOAD` klickst.

{% include image.html image=page.image2 %}

In deinem Downloads-Ordner sollte eine Arduino.app-Datei erscheinen. Verschiebe diese Datei in deinen "Programme"-Ordner. Durch Öffnen der Datei `Arduino.app` kann die IDE gestartet werden. Im zweiten Schritt muss noch das [Board Support Package installiert werden](/arduino/board-support-package-installieren/), um die senseBox MCU programmieren zu können.


## Arduino IDE für Linux herunterladen

Die senseBox ist ein Microcontroller mit verschiedenen Komponenten und Sensoren. Sie wird über die Entwicklungsumgebung _Arduino IDE_ programmiert. Lade die Version aktuellste Version (1.8.15 - Stand Juni 2021) von der [Arduino Homepage](https://www.arduino.cc/en/software)  herunter:

{% include image.html image=page.image1 %}

Arduino ist ein Open-Source Projekt und wird durch Spenden finanziert. Daher wirst du vor dem Download nach einer Spende gefragt; das kannst du überspringen, indem du auf `JUST DOWNLOAD` klickst.

{% include image.html image=page.image2 %}

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
Um den Arduino programmieren zu können, sind unter Ubuntu 14 & 16 zusätzliche Rechte notwendig. Diese können für den/die aktuelle/n Nutzer:in mit den folgenden Befehlen eingerichtet werden \(benötigt Admin-Rechte\):

Führe `udevadm monitor --udev` aus und schließe den Arduino per USB an, um die Device-ID zu bestimmen. Die angegebene Bezeichnung am Ende der Ausgabe \(zB. `ttyUSB0`\) ist die Device-ID. Beende `udevadm` per `ctrl+C`, und führe noch die folgenden Befehle aus, wobei die herausgefundene Device-ID eingesetzt werden muss:

```text
sudo usermod -a -G dialout $(whoami)
sudo chmod a+rw /dev/<device-id>
```

Nach einem Logout und erneutem Login sollte der Arduino aus der Arduino IDE programmierbar sein!



