---
set: erste-schritte-arduino
resources:
  - name: Arduino
    link: https://www.arduino.cc
  - name: Arduino Old Releases
    link: https://www.arduino.cc/en/Main/OldSoftwareReleases#previous
title_order: 2
date: 2020-03-11
set_order: 3
image1: /images/2020-03-11-allgemein-arduino-ide-installieren/arduino-download.png
image2: /images/2020-03-11-allgemein-arduino-ide-installieren/arduino-donate.png
type: Document
title: Installation der Arduino IDE
description: Installation der Arduino IDE
categories: arduino
---
Die senseBox ist ein Microcontroller mit verschiedenen Komponenten und Sensoren. Sie kann über die Entwicklungsumgebung *Arduino IDE* programmiert werden. Bevor du die senseBox über die Arduino IDE programmieren kannst, musst du Treiber sowie eine Software auf deinem Computer installieren.

Schau dir die Anleitung für dein Betriebsystem an und folge den angegebenen Schritten.

## Arduino Software für Windows herunterladen

 Lade die neueste Version 2.0.0 oder höher von der [Arduino Homepage](https://www.arduino.cc/en/software) herunter:

{% include image.html image=page.image1 %}

>  	Lade bitte die zip-Datei herunter und <b> nicht </b> den Windows-Installer, um mögliche Probleme zu vermeiden!

Arduino ist ein Open-Source Projekt und wird durch Spenden finanziert. Daher wirst du vor dem Download nach einer Spende gefragt; falls du nichts spenden möchtest, kannst du auf `JUST DOWNLOAD` klicken.

{% include image.html image=page.image2 %}

Lege auf deiner Festplatte einen neuen Ordner an und entpacke darin die zip-Datei. Durch das Ausführen der Datei `arduino.exe` kann die IDE gestartet werden.  

## Arduino Software für Mac(OSX) herunterladen

Lade die Version 2.0.0 von der [Arduino Homepage](https://www.arduino.cc/en/Main/OldSoftwareReleases#previous) herunter:

{% include image.html image=page.image1 %}

Arduino ist ein Open-Source Projekt und wird durch Spenden finanziert. Daher wirst du vor dem Download nach einer Spende gefragt; das kannst du überspringen, indem du auf `JUST DOWNLOAD` klickst.

{% include image.html image=page.image2 %}

In deinem Downloads-Ordner sollte eine Arduino.app-Datei erscheinen. Verschiebe diese Datei in deinen "Programme"-Ordner. Durch Öffnen der Datei `Arduino.app` kann die IDE gestartet werden. 

## Arduino Software für Linux herunterladen

Lade die Version 2.0.0 von der [Arduino Homepage](https://www.arduino.cc/en/Main/OldSoftwareReleases#previous) herunter:

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
tar -xvf arduino-2.0.0-linux64.tar.xz
cd arduino-2.0.0
./install.sh
```

Um den Arduino programmieren zu können, sind unter Ubuntu 14 & 16 zusätzliche Rechte notwendig. Diese können für den/die aktuelle/n Nutzer:in mit den folgenden Befehlen eingerichtet werden (benötigt Admin-Rechte):

Führe `udevadm monitor --udev` aus und schließe den Arduino beziehungsweise die senseBox per USB an, um die Device-ID zu bestimmen. Die angegebene Bezeichnung am Ende der Ausgabe (zB. `ttyUSB0`) ist die Device-ID. Beende `udevadm` per `ctrl+C`, und führe noch die folgenden Befehle aus, wobei die herausgefundene Device-ID eingesetzt werden muss:

```text
sudo usermod -a -G dialout $(whoami)
sudo chmod a+rw /dev/<device-id>
```

Nach einem Logout und erneutem Login sollte ein Arduino oder die Sensebox aus der Arduino IDE programmierbar sein!

Für letzteres kann nun das [Board-Support-Package installiert](https://docs.sensebox.de/arduino/board-support-package-installieren/) werden.