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


