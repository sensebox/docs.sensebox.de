---
date: 2020-03-11
title: Erste Schritte
categories: Blockly
description: Verwendung von Blockly für die senseBox
type: Document
video_id: jzlOJ7Zuqqw
sets: blockly
set_order: 1
resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
---


## Verwendung

[Blockly für senseBox](https://blockly.sensebox.de) ist eine grafische Programmieroberfläche für die senseBox. Die Oberfläche läuft in allen gängigen Browsern und benötigt keine Softwareinstallation.

## Code compilieren und übertragen

Ist dein Programm fertig kannst du es mit einem Klick auf den orangenen “Kompilieren”-Button oben rechts herunterladen.

Verbinde zuerst die MCU mit Hilfe des USB-Kabels mit deinem Computer. Die senseBox MCU hat zwei verschiedene Modi: Den Programm- und den Lern-Modus. Standardmäßig befindet sich die MCU im Programm-Modus. In diesem führt sie das zuletzt übertragende Programm aus. Du erkennst den Program-Modus daran, dass die LED auf der MCU grün leuchten. Bevor nun ein neues Programm übertragen weren kann, muss die MCU in den Lern-Modus versetzt werden. Dies geschieht durch einen Doppelklick auf den roten “Reset”-Button auf der MCU. Du erkennst den Lern-Modus daran, dass nur eine LED direkt neben der “Reset”-Knopf rot leuchtet. Im Lern-Modus wird die senseBox außerdem als Wechseldatenträger erkannt.

{% include youtube.html video_id=page.video_id %}