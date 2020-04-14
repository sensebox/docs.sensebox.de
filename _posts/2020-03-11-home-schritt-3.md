---
date: 2020-03-11
title: "Schritt 3: Programmcode übertragen"
title_order: 3
categories: aufbau-sensebox-home
description: Schritt 3 zum Aufbau der senseBox:home
type: Document
set: aufbau-sensebox-home
set_order: 3
---

## Online kompilieren
Der einfachste Weg deinen Code auf die senseBox zu bekommen ist unseren Online Compiler zu benutzen. Dafür musst du in der Maske einige Angaben machen. Wenn etwas nicht auf deinen individuellen Aufbau der senseBox passt, kannst du das Feld einfach frei lassen. Zum Abschluss drückst du auf "Kompilieren" und eine Datei im Format .BIN wird von deinem Browser heruntergeladen. 
![Konfiguration um Online zu kompilieren](https://github.com/sensebox/resources/raw/master/gitbook_pictures/202003-online-compiling.PNG)

### Übertragen auf die senseBox MCU

Schließt du deine senseBox MCU an deinen Computer an und führst einen Doppelklick auf den roten Button aus, wird diese als Wechseldatendräger erkannt. Mit einem Klick auf "Code Kompilieren" in der Weboberfläche wird dein Programmcode auf dem Server kompiliert und eine .BIN Datei wird dir zum Download angeboten. Je nachdem welches Betriebssystem du verwendest, unterscheidet sich nun der Kopiervorgang. 

#### Kopieren unter Windows 

Unter Windows kannst du die erstellte .BIN Datei einfach per Drag & Drop auf den Wechseldatenträger <b>SENSEBOX</b> kopieren. Die rote LED am Button wird kurz flackern und anschließend startet das Board selbstständig neu und führt deinen Programmcode aus. 
___________

#### Kopieren unter MacOS

Unter MacOS funktioniert das Kopieren der .BIN per Drag & Drop leider zurzeit noch nicht. Eine Möglichkeit ist die Datei im Terminal per dd-Befehl zu kopieren (nur erfahrenen Nutzern zu empfehlen!) oder einen alternativen Dateimanager wie zum Beispiel [muCommander](http://www.mucommander.com/) zu verwenden.
___________


#### Kopieren unter Linux 

Unter Linux kannst du die erstellte .BIN Datei einfach per Drag & Drop auf den Wechseldatenträger <b>SENSEBOX</b> kopieren. Die rote LED am Button wird kurz flackern und anschließend startet das Board selbstständig neu und führt deinen Programmcode aus. 
___________

<hr>

<a href="/aufbau-sensebox:home/home-schritt-2/" class="button">Zurück zu Schritt 2</a>