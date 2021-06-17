---
date: 2020-03-11
title: Editoren für die senseBox
title_order: 4
categories:  misc
description: Übersicht über die verschiedenen Editoren der senseBox
type: Document
resources:
  - name: "Blockly für senseBox"
    link: https://blockly.sensebox.de
  - name: "Arduino IDE"
    link: https://www.arduino.cc/
  - name: "openRoberta"
    link: https://lab.open-roberta.org/
  - name: "CircuitPython für die senseBox MCU"
    link: https://circuitpython.org/board/sensebox_mcu/
image1: /images/2020-03-11-sensebox-editoren/blockly.png
image2: /images/2020-03-11-sensebox-editoren/arduino.png
image3: /images/2020-03-11-sensebox-editoren/nepo.png
image4: /images/2020-03-11-sensebox-editoren/circuitpython.png
---

Die senseBox kann mithilfe von vier verschiedenen Editoren programmieren werden. 

## Blockly für senseBox

Mit [Blockly für senseBox](https://blockly.sensebox.de/ardublockly/?board=sensebox-mcu) kannst du deine senseBox MCU über eine grafische Programmieroberfläche programmieren. Auf dem Computer muss keine Software installiert werden und du kannst direkt loslegen. 

{% include image.html image=page.image1 %}


## Arduino IDE

Die Arduino IDE kannst du auf der Website von Arduino <a href="https://arduino.cc/downloads">kostenlos herunterladen</a>. Die Arduino IDE bietet dir den kompletten Zugriff auf alle Funktionen, die die Programmiersprache Arduino bereithält. Über die Arduino IDE kannst du auch zusätzliche Sensoren und Bauteile, die nicht in Blockly für senseBox oder Open Roberta enthalten sind, programmieren. Die Arduino IDE muss auf dem Computer installiert werden. Zusätzlich muss ein Board Support Package für die senseBox MCU heruntergeladen werden. Wie genau das funktioniert, erfährst du [hier](/allgemein/board-support-package-installieren/).

{% include image.html image=page.image2 %}


## Open Roberta

openRoberta ist eine weitere Möglichkeit die senseBox zu programmieren. Das openRoberta lab benötigt keine Installation auf deinem Computer und bietet einen ähnlichen Funktionsumfang wie Blockly für senseBox. Eine kurze Einführung in die Verwendung der senseBox in openRoberta findest du [hier](/allgemein/allgemein-einfuehrung-openroberta/).

{% include image.html image=page.image3 %}

## CircuitPython

Die senseBox MCU kann auch über Circuit Python programmiert werden. CircuitPython benötigt einen angepassten Bootloader, der einfach auf die senseBox MCU kopiert werden kann. Mehr Informationen zur Verwendung von CircuitPython mit der senseBox MCU findest du [hier](/misc/circuitpython/)

{% include image.html image=page.image4 %}