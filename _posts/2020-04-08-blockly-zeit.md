---
date: 2020-04-07
title: Zeit
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



## Programmcode unterbrechen


{% include image.html image=page.image1 %}

Mit diesem Block kannst du deinen Programmcode für eine gewisse Zeit unterbrechen. In dieser Zeit pausiert der Mikrokontroller und es werden keine Aktionen ausgeführt. Die Zeit wird in Millisekunden angegeben (1 Sekunde = 1000 Millisekunden)


Dieser Block hat die gleiche Funktion wie der vorherige Block, allerdings wird hier eine Zeit in Mikrosekunden angegeben.


## Bereits vergangene Zeit 

Dieser Block gibt dir die Zeit, die dein Programmcode bereits läuft. Die Laufzeit wird in Millisekunden angegeben

Auch mit diesem Block wird dir die Laufzeit seit dem Start deines Programmes angegeben, diesmal allerdings in Mikrosekunden.



## Warte für immer

Mit diesem Block kannst du dein Programm einfach beenden lassen.

## Messintervall

Damit das Übertragen der Messwerte nicht jede Sekunde erfolgt, sondern erst nach einem gewissen Zeitintervall, kannst du diesen

Block verwenden. Ziehe dazu alle Aktionen, die erste nach einer gewissen Zeit erfolgen sollen in die Schleife und trage die Zeit in Millisekunden ein. 
