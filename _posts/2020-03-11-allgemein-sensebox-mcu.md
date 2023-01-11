---
date: 2020-03-11
title: Die senseBoxMCU
categories: hardware
description: Die senseBox MCU
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.kaufen/product/sensebox-mini
image1: /images/2020-03-11-allgemein-sensebox-mcu/mcu_one_top.png
image2: /images/2020-03-11-allgemein-sensebox-mcu/mcu_comparison.jpeg
image3: /images/2020-03-11-allgemein-sensebox-mcu/mcu_v13.jpeg
image4: /images/2020-03-11-allgemein-sensebox-mcu/mcu_v15.jpeg
image5: /images/2020-03-11-allgemein-sensebox-mcu/mcu_v15_bmx.jpeg
---

Der senseBox-Microcontroller ist speziell für die Bedürfnisse der senseBox entwickelt. Deshalb hat der Microcontroller insbesondere drei Eigenschaften: er ist schnell, energiesparend und hat einen großen Programmspeicher.

Auch ohne Vorkenntnisse kann der Microcontroller ganz einfach mit der Übertragung eines vorgefertigten Sketches in 10 Minuten "programmiert" werden. Für fortgeschrittene Programmierer kann wie gewohnt die Arduino IDE eingesetzt werden, um neue und individuelle Projekte durchzuführen.

{% include image.html image=page.image1 %}

## Technische Spezifikationen

### Prozessor
Der Prozessor basiert auf dem ARM Cortex-M0+ Prozessor aus der SAM D21 Familie von Microchip.

### Schnittstellen
Sensoren und Aktoren werden über die bewährten Schnittstellen wie I2C, UART und digitale I/Os mit einem robusten JST-Steckersystem angesprochen (5V tolerant). 

### Datenübertragung
Über die beiden XBee kompatiblen Sockel werden UART oder SPI Module angeboten. Wahlweise kann die Datenübertragung dadurch per WLAN, LAN oder LoRa in Echtzeit durchgeführt werden. Alternativ können die Daten auch auf einer Mikro-SD Karte gespeichert werden.  

## Programmierung

Die senseBox MCU kann über verschiedene Programmierumgebungen programmiert werde. Eine genaue Übersicht findest du [hier](/arduino/allgemein-sensebox-editoren/).


## Revisionen der senseBox MCU

Während der Entwicklung der senseBox MCU wurden mehrere Revisionen entwickelt. Die aktuelle Version ist die V1.5. Die folgende Übersicht zeigt dir die Unterschiede zwischen den einzelnen Revisionen. Grundlegend sind alle Versionen kompatibel zu den anderen Versionen und unterscheiden sich nur geringfügig in der Hardware.


{% include image.html image=page.image2 %}

### V1.3

Die Revision 1.3 ist die erste Version die ab 2018 ausgeliefert wurde. Sie ist mit einem Beschleunigungssensor (BMX055) ausgestattet und Mikro USB Anschluss ausgestattet. 


{% include image.html image=page.image3 %}

### V1.5 mit USB-C Anschluss

Die Version 1.5 der senseBox MCU ist mit einem USB-C Anschluss ausgestattet. Dieser ermöglicht eine einfache und schnelle Verbindung zum Computer. Die Version 1.5 ist kompatibel zu allen bisherigen Versionen der senseBox MCU. 


{% include image.html image=page.image4 %}

Aufgrund der Knappheit von Elekronikbauteilen wurde eine Charge der Revision 1.5 ohne Beschleunigungssensor (BMX055) ausgeliefert. Falls du dir unsicher bist ob deine senseBox MCU eine Beschleunigungssensor hat, hilft dir die untstehende Grafik weiter. Die obere Version der MCU V1.5 hat einen Beschleunigungssensor, die untere Version nicht.

{% include image.html image=page.image5 %}