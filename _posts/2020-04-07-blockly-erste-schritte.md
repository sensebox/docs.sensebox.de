---
date: 2020-03-11
title: Getting started
title_order: 1
categories: Blockly
description: Verwendung von Blockly für die senseBox
type: Document
video_id: jzlOJ7Zuqqw
set: blockly-erste-schritte
set_order: 1
resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-03-11-blockly-erste-schritte/block_export.svg
image2: /images/bloques (3).svg
---


## Vorbereitungen
### Am Computer
Um die senseBox Programmieren zu können, benötigst du das mitgelieferte USB-Kabel, einen Computer und Zugang zum Internet. 
Öffne in deinem Internetbrowser nun die Website [Blockly für senseBox](https://blockly.sensebox.de/) und wähle deine Box aus. Nun kannst du dein eigenes Programm ohne Softwareinstallation schreiben. Ist dein Programm fertig kannst du es mit einem Klick auf den orangenen "Kompilieren"-Button oben rechts herunterladen. Standardmäßig wird es als .BIN-Datei im "Downloads" Ordner gespeichert.

{% include image.html image=page.image1 %}

### An der senseBox MCU
Verbinde zuerst die MCU mit Hilfe des USB-Kabels mit deinem Computer.
Die senseBox MCU hat zwei verschiedene Modi: Den Programm- und den Lern-Modus. Standardmäßig befindet sich die MCU im Programm-Modus. In diesem führt sie das zuletzt übertragende Programm aus. Du erkennst den Program-Modus daran, dass die LEDs auf der MCU grün leuchten.
Bevor nun ein neues Programm übertragen weren kann, muss die MCU in den Lern-Modus versetzt werden. Dies geschieht durch einen Doppelklick auf den roten "Reset"-Button auf der MCU. 

{% include image.html image=page.image2 %}

{% include youtube.html video_id=page.video_id %}

Du erkennst den Lern-Modus daran, dass nur eine LED direkt neben der "Reset"-Knopf rot leuchtet. Im Lern-Modus wird die senseBox außerdem als Wechseldatenträger erkannt.

## Übertragen
Befindet sich deine senseBox MCU im Lern-Modus kannst du deinen Sketch aus dem "Download"-Ordner einfach auf den Wechseldatenträger "SENSEBOX" kopieren.

![Ein Programm auf den senseBox kopieren](https://raw.githubusercontent.com/sensebox/sensebox.github.io/Projects_basics/images/projects/BASICS/copy_to_mcu.gif)