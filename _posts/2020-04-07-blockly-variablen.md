---
date: 2020-03-11
title: Variablen
title_order: 6
categories: Blockly
description: Arbeiten mit Variablen in Blockly
type: Document
set: blockly-erste-schritte
set_order: 6
resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-04-08-blockly-variablen/blockly-variablen-1.svg
image2: /images/2020-04-08-blockly-variablen/blockly-variablen-2.svg
image3: /images/2020-04-08-blockly-variablen/blockly-variablen-3.svg
image4: /images/2020-04-08-blockly-variablen/blockly-variablen-4.svg
---

## Allgemeines
Variablen sind Platzhalter für Zahlen, Buchstaben und Zeichenketten. Das bedeutet, dass eine Variable **nicht** über den gesamten Programmverlauf gleich bleiben muss. Dies ist besonders dann praktisch, wenn du eine bestimmt Information an verschiedenen Stellen im Programm nutzen möchtest.

Variablen lassen sich durch den `Schreibe Element`-Block definieren.

{% include image.html image=page.image1 %}

Im Drodown-Menü des Blocks lässt sich die Variable umbenennen und eine neue Variable erstellen.

## Beispiel
Nach einem Fussballspiel soll in einer Variable gespeichert werden, wieviele Tore gefallen sind. Diese Variable wird dann auf dem Display angezeigt

{% include image.html image=page.image2 %}

Um das einfache Beispiel etwas zu erweitern, sollen nun live Punkte dazugezählt werden können. Für jedes gefallene Tor muss der eingebaute Knopf auf der MCU einmal gedrückt werden.

{% include image.html image=page.image3 %}

## Datentypen
Je nachdem was in einer Variable gespeichert werden sollte man den richtigen Datentyp festlegen. Den Datentyp legst du mit Hilfe des `als Zeichen`-Blocks fest. Dieser Block wird an einen `Schreibe Element`-Block angeknüpft. Anschließend wird im freien Blockabschnitt wird der zu speichernde Wert eingefügt und im Dropdown-Menü der Datentyp gewählt.

{% include image.html image=page.image4 %}
<br>

In Blockly gibt es folgende Datentypen:

**Zeichen:**     Für einzelne Textzeichen

**Text:**        Für ganze Wörter oder Sätze

**Boolean:**     Für Werte die entweder wahr oder falsch sind (bzw. 1 oder 0)

**kurze Zahl:**  Für einstellige Zahlen

**Zahl:**        Für ganze Zahlen von -32.768 bis 32.767

**große Zahl:**  Für große Zahlen von -2.147.483.648 bis 2.147.483.647

**Dezimalzahl:** Für Kommazahlen    
