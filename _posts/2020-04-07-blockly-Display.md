---
date: 2020-04-07
title: Display  
categories: Blockly
description: Verwendung des Displays der senseBox
type: Document
sets: blockly-erste-schritte
set_order: 3
resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
---
In der senseBox ist ein OLED-Display enthalten. Dieses kann benutzt werden um z.B. Text, Messwerte oder Graphen anzeigen zu lassen.
Das Display hat eine Auflösung von 128x64 Pixeln. Das heißt 128 Pixel in horizontaler Ebene (x-Achse) und 64 Pixel in vertikaler Ebene (y-Achse). 

![Display](/images/2020-04-07-blockly-display/Display.png)

Um Informationen auf dem Display anzeigen zu lassen muss dieses zuerst im `Setup()` initalisiert werden. Anschließend können in der `Endlosschleife()` die `Zeige auf dem Display`-Schleife und der `Display löschen`-Block platziert werden. Im freien Abschnitt des `Zeige auf Display`-Blocks kann dann anschließend festgelegt werden, was genau angezeigt werden soll. Der `Display löschen`-Block muss hinzugefügt werden, damit verschiedene Informationen nicht übereinander geschrieben werden.

![Display](/images/2020-04-07-blockly-display/blockly-Display-1.png)

## Text/Zahl anzeigen
Um Text oder eine Zahl anzeigen zu lassen ziehe den `Schreibe Text/Zahl`-Block in den freien Abschnitt des `Zeige auf Display`-Blocks.