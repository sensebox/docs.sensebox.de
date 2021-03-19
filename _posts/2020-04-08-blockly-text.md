---
date: 2020-04-07
title: Text
title_order: 10
categories: Blockly
description: Grundlagen zur Kategorie Text
type: Document

resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-04-08-blockly-text/blockly-text-1.svg
image2: /images/2020-04-08-blockly-text/blockly-text-2.svg
image3: /images/2020-04-08-blockly-text/blockly-text-3.svg
image4: /images/2020-04-08-blockly-text/blockly-text-4.svg
image5: /images/2020-04-08-blockly-text/blockly-text-5.svg
image6: /images/2020-04-08-blockly-text/blockly-text-6.gif
---

## Textfeld
Mit dem Textfeld Block `" "` kannst du Text erstellen. Schreibe den gewünschten Text dazu in das Feld zwischen den Anführungszeichen. 

{% include image.html image=page.image1 %}

## Erstelle Text aus
Mit dem `Erstelle Text aus`-Block kannst du einerseits Messwerte in Text umwandeln und andererseits zusammengesetze Texte (aus mehreren Textfeldern, Zahlen, Messwerten oder Variablen) erstellen. 

{% include image.html image=page.image2 %}

Der normale Erstelle-Text-Aus-Block kann mit einem Klick auf das Zahnrad erweitert werden. Du kannst noch weitere Elemente durch Klicken und Ziehen hinzufügen, um Text aus mehreren Elementen zu erstellen. Nach dem Bearbeiten kann mit einem weiteren Klick auf das Zahnrad das Fenster wieder geschlossen werden. 

{% include image.html image=page.image6 %}
## Text anhängen

Mit dem `Text anhängen`-Block kannst du Text an eine bestehende Variable anhängen.

{% include image.html image=page.image3 %}

## Länge

Mit dem `Länge`-Block kannst du dir die Länge eines Textblocks ausgeben lassen.

{% include image.html image=page.image4 %}

> Der Textblock "senseBox" wäre zum Beispiel 8 Einheiten lang.

## ist leer?

Mit dem `ist leer?`-Block kannst du überprüfen, ob ein gegebener Textblock leer ist (die Länge 0 hat). Das Ergebnis ist entweder wahr (wenn der gegebene Textblock tatsächlich leer ist) oder falsch (wenn sich Zeichen im Textblock befinden). 

{% include image.html image=page.image5 %}
