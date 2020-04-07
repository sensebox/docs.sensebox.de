---
date: 2020-04-07
title: Dein erster Sketch
title_order: 2 # Indicates the order of apperance on the overview pages
categories: Blockly
description: Schreibe dein erstes Programm für die senseBox
type: Document
set: blockly-erste-schritte
set_order: 2
resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
---

Um Blockly etwas kennenzulernen schreibst du ein einfaches Programm, welches die eingebaute LED auf der senseBox blinken lässt.

## Programmierung

### Schritt 1: Setup und Endlosschleife

Dieser Block wird direkt beim Starten der Oberfläche geladen und sollte immer verwendet werden. Die zwei Basisfunktionen `Setup()` und `Endlosschleife()` werden immer benötigt, um ein funtkionsfähiges Programm zu schreiben.
Alle Blöcke, die innerhalb der `Setup()`-Funktion stehen, werden nur zu Beginn des Programmes einmal ausgeführt. In dieser Funktion wird zum Beispiel das Display initialsiert oder die WLAN Verbindung hergestellt. Alle Blöcke, die innerhalb der `Endlosschleife()` stehen, werden fortlaufend ausgeführt. Der Mikrocontroller führt hierbei alle Blöcke immer wieder von oben nach unten hin aus. In der `Endlosschleife()` werden zum Beispiel die Sensoren ausgelesen oder auch die Messwerte auf SD-Karte gespeichert oder ins Internet übertragen.

![Basisblock](https://raw.githubusercontent.com/sensebox/sensebox.github.io/Projects_basics/images/projects/ES_ersterSketch/setup_loop.png)

### Schritt 2: Die eingebaute LED einschalten

Um die eingebaute LED anzuschalten, musst du den `LED an digital`-Block in die Endlosschleife ziehen. Anschließend wählst du unter PIN "BUILTIN_1" und unter Status "Ein" aus.

![Eingebaute LED einschalten](https://raw.githubusercontent.com/sensebox/sensebox.github.io/Projects_basics/images/projects/ES_ersterSketch/builtin1_on.png)

Die eingebaute LED findest du über dem roten Reset-Knopf auf der senseBox MCU.


### Schritt 3: Die eingebaute LED blinken lassen

Um die eingebaute LED blinken zu lassen, ist es nötig, sie mit einem weiteren `LED an digital` Block wieder auszuschalten. Zusätzlich muss nach dem An- sowie Ausschalten eine Pause eingefügt werden, damit das Blinken überhaupt sichtbar ist. Den `Warte` Block findest du in der Kategorie `Zeit`.

![Eingebaute LED blinken lassen](https://raw.githubusercontent.com/sensebox/sensebox.github.io/Projects_basics/images/projects/ES_ersterSketch/builtin1_blink.png)

<div class="panel panel-info">
  <div class="panel-heading">
1000 Millisekunden sind 1 Sekunde
  </div>
  <div class="panel-body">
  </div>
</div>