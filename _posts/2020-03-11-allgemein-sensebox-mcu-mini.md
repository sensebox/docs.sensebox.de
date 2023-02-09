---
date: 2020-03-11
title: Die senseBox MCU:mini
categories: hardware
description: Die senseBox MCU:mini
type: Document
resources:
  - name: "Shop: senseBox Mini V2"
    link: https://sensebox.kaufen/product/sensebox-mini-v2
  - name: "Shop: senseBox MCU:mini"
    link: https://sensebox.kaufen/product/sensebox-mcu-mini
image1: /images/2020-03-11-allgemein-sensebox-mcu-mini/mcu_mini_01.jpeg
image2: /images/2020-03-11-allgemein-sensebox-mcu-mini/mcu_mini_02.jpeg
---

Der senseBox-Microcontroller mini ist eine miniaturisierte Version der senseBox MCU, bietet aber trotzdem zahlreiche Möglichkeiten zur Datenerhebung. Durch die Reduzierung der Anzahl und Verkleinerung der Anschlüsse, die beidseitige Bestückung und die direkte Integration von Bauteilen auf der MCU mini konnte die Größe der Platine auf ca. 20% der bisherigen Größe reduziert werden. 


{% include image.html image=page.image1 %}
{% include image.html image=page.image2 %}

Die MCU:mini kann über [Blockly](https://blockly.sensebox.de) ohne Vorkenntnisse “programmiert” werden. Für fortgeschrittene Programmierer kann wie gewohnt die Arduino IDE oder der in Blockly integrierte [Code-Editor](https://blockly.sensebox.de/codeeditor) eingesetzt werden, um neue und fortgeschrittenere Projekte durchzuführen.

## Technische Spezifikationen

### Prozessor
Der Prozessor basiert auf dem ARM Cortex-M0+ Prozessor aus der SAM D21 Familie von Microchip.

### Schnittstellen
Zwei I2C Anschlüsse mit kleinerem, verkettbaren Qwiic Connector ermöglichen den Anschluss von Sensoren und weiteren Bauteilen. Eine RGB-LED befindet sich direkt auf dem Board. 

#### Anschlüsse
- 2 I2C (QWICC)
- 1 UART
- 1 I/O (zwei digital/analog Pins, 5V sowie GND)
- 1 Lüfteranschluss (GND/5V)

#### Stromversorgung
Die MCU:mini kann über die USB-C Anschluss sowohl programmiert als auch dauerhaft mit Strom versorgt werden.

### Datenübertragung
Der Mikrocontroller bietet einen XBEE-Steckplatz zur Verwendung der Datenübertragungsmodule. Das Modul für Mikro-SD Karten ist ist direkt auf der MCU integriert.

## Programmierung

Die senseBox MCU:mini kann über verschiedene Programmierumgebungen programmiert werden. Eine genaue Übersicht findest du [hier](/arduino/allgemein-sensebox-editoren/).


