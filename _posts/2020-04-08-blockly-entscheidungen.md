---
date: 2020-04-07
title: Entscheidungen
title_order: 5
categories: Blockly
description: Erste Schritte Entscheidungen
type: Document
set: blockly-erste-schritte
set_order: 5
resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-04-08-blockly-entscheidungen/blockly-entscheidungen-1.svg
image2: /images/2020-04-08-blockly-entscheidungen/blockly-entscheidungen-2.svg
image3: /images/2020-04-08-blockly-entscheidungen/blockly-entscheidungen-3.svg
image4: /images/2020-04-08-blockly-entscheidungen/blockly-entscheidungen-4.svg
---

## Allgemeines
Entscheidungen oder Verzweigungn in Programmen gehören zu den wichtigsten Kontrollstrukturen beim Programmieren. Sie ermöglichen dir dein Programm auf verschiedene

## Wenn, mache Beziehung
Der `wenn, mache`-Block verfügt über zwei freie Blockabschnitte `wenn` und `mache`.

{% include image.html image=page.image1 %}

Die Aktionen, die am freien Blockabschnitt `mache` angeknüpft sind, werden nur dann ausgeführt, wenn die am Blockabschnitt `wenn` angeknüpfte Bedingung erfüllt ist. 

Zum Beispiel soll die eingebaute LED auf der senseBox MCU eingeschaltet werden, **wenn* der eingebaute Button gedrückt wird.

{% include image.html image=page.image2 %}

Befehle, die nach dem `wenn, mache`-Block hinzugefügt wurden, werden auf jeden Fall ausgeführt, auch wenn die Bedingung zuvor nicht erfüllt wurde.

## Sonst
Mit einem Klick auf das kleine Zahnrad oben links im `wenn, mache`-Block kannst du den Block um einen `sonst`-Blockabschnitt erweitern. Befehle die in diesem Blockabschnitt abgelegt werden, werden nur dann ausgeführt wenn die Bedingung zuvor **nicht** erfüllt wurde. Wurde die Bedingung erfüllt, werden sie übersprungen.

Zum Beispiel soll hier die eingebaute LED 1 nur dann leuchten, **wenn** der eingebaute Button gedrückt wird und **sonst** die eingebaute LED 2.

{% include image.html image=page.image3 %}

## Verzweigungen
Mit einem Klick auf das kleine Zahnrad oben links im `wenn, mache`-Block kannst du den Block um einen `sonst wenn`-Blockabschnitt erweitern. Nun wird zuerst die oberste `wenn` Bedingung überprüft, sollte diese nicht erfüllt sein wird die darauf folgende `sonst wenn` Bedingung überprüft. So werden nur die Befehle ausgeführt, deren zugehörige Bedingung erfüllt ist.
Im Vergleich zur `sonst` Bedingung kannst du so mehr als zwei Bedingungen festlegen. 

Zum Beispiel soll je nach Temperatur eine LED angeschaltet werden. Bei Temperaturen unter 0°C soll LED 1, bei genau 0°C LED 2 und bei Temperaturen über 0°C LED 3 angeschaltet werden.

{% include image.html image=page.image4 %}
