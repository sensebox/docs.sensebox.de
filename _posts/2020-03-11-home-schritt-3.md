---
date: 2020-03-11
title: senseBox:home Schritt 3
categories: senseBox:home
description: Schritt 3 zum Aufbau der senseBox:home
type: Document
set: aufbau-sensebox-home
set_order: 3
---

Um die gemessenen Daten auf die openSenseMap zu übertragen, musst du dich dort zuerst registrieren und eine neue senseBox anlegen. Wie das geht, erfährst du im folgenden Abschnitt.

Die openSenseMap ist eine Plattform um Sensordaten zu speichern, zu vergleichen und zu visualisieren. Schau sie dir doch am besten mal an. Gehe auf [www.opensensemap.org](https://www.opensensemap.org) und entdecke einen riesigen Pool an Sensordaten aus der ganzen Welt. Nicht nur senseBoxen senden Daten an die openSenseMap, sondern auch andere Microcontroller mit Sensoren. Wie die einzelnen Funktionen der openSenseMap und ihre Schnittstellen funktionieren, findest du [hier](https://sensebox.github.io/books-v2/osem).

## 1. Nutzeraccount Registrierung
Gehe auf [www.opensensemap.org](https://www.opensensemap.org) und lege dir einen Account an. Dafür klickst du rechts oben in der Ecke auf "Login" und gehst dann auf "Sign up". Du brauchst zum Registrieren eine gültige E-Mail-Adresse. Nach erfolgreicher Registrierung erhältst du eine E-Mail mit einem Bestätigungslink. Bitte klicke den Link, um die Registrierung abzuschließen. 

![Account anlegen](https://github.com/sensebox/resources/raw/master/gitbook_pictures/Sing_up.PNG)

## 2. Eine neue senseBox anlegen
Nach der erfolgreichen Registrierung kannst du damit beginnen deine senseBox anzulegen. Klicke dafür auf "New senseBox / Neue senseBox" in deinem Menü und bestätige die Nutzungsbedingungen. Befolge danach die Anweisungen der Registrierung und gebe folgende Daten an:

* Einen frei wählbaren Namen der senseBox
* Die Umgebung (Exposure), in der du deine senseBox aufstellen möchtest
* Den Ort (Location), an dem du deine senseBox aufstellen möchtest (du kannst deinen Standort auch automatisch bestimmen lassen)

Da die openSenseMap offen für alle Arten von senseBoxen ist, wirst du nach der verwendeten Hardware gefragt. Wähle *senseBox:home V2* und den Bee den du verwendest (WiFi, oder Ethernet)

![Auswahl von senseBox:home V2 MCU und WiFi Internetverbindung](https://github.com/sensebox/resources/raw/master/gitbook_pictures/202003-screen-registration.PNG)

<div class="box_info">
    <i class="fa fa-info fa-fw" aria-hidden="true" style="color: #42acf3;"></i>
Du bist dir nicht sicher ob du ein Ethernet oder WiFi-Bee hast, oder kannst den Unterschied zwischen dem Luftdruck und Temperatursensor nicht erkennen? Im Kapitel <a href = "../komponenten/README.md">Komponenten</a> findest du Bilder und weitere Hinweise zu den einzelnen Bauteilen.
</div>


Möchtest du deine Daten über LoRa an die openSenseMap schicken, wählst du bei "Verbindungsart" LoRa aus. Anschließend kannst du im Reiter "Erweitert" deine Lora Einstellungen angeben. Hier musst du die Application-ID und Device-ID angeben, welche du beim <a href="www.thethingsnetwork.org">TheThingsNetwork</a> angegeben hast. 
![LoRa Konfigurationen](https://github.com/sensebox/resources/raw/master/gitbook_pictures/LoRaOSEM.PNG)


Jetzt hast du es fast geschafft! Noch schnell die Sensoren auswählen, welche du an deine senseBox anschließen wirst. Einfach anklicken und fertig. Bei einigen Sensoren musst du noch angeben an welchen Ports auf dem Mikrocontroller diese angeschlossen sind. Danach kannst du den Vorgang abschließen.

## 3. Summary der Registrierung und Mail erhalten
Wenn du die Registrierung abgeschlossen hast, musst du noch einmal der Veröffentlichung deiner Daten zustimmen. Danach erhälst du eine Summary deiner Registrierung. Dort wird dir deine senseBox ID, deine Sensoren-IDs und der Arduino Code angezeigt.  

![Summary der Registrierung. Hier siehst du die IDs deiner senseBox und deiner Sensoren!](https://github.com/sensebox/resources/raw/master/gitbook_pictures/202003-overview.PNG)


Die senseBox ID ist ein eindeutiger Identifikator deiner senseBox. Damit kannst du deine senseBox z.B. über die URL finden (opensensemap.org/explore/HIER-DEINE-SENSEBOX-ID-EINGEBEN) oder in Datensätzen aufspüren. Des Weiteren wird sie für verschiedene Applications und Funktionen rund um die senseBox und die openSenseMap verwendet.


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


### Arduino-Code auf die senseBox laden
Nachdem du den ```.ino``` Anhang der Email heruntergeladen hast (oder weiter unten in der Übersicht kopiert hast), muss dieses Programm auf deine senseBox geladen werden. Dafür musst du natürlich die Arduino IDE (wie in Schritt 1 erklärt) auf deinem Computer heruntergeladen haben. In Kurzfassung kannst du danach folgende Schritte befolgen:

### WiFi-Bee

* Arduino Anwendung öffnen
* In der Menüleiste ``Datei`` → ``Öffnen`` auswählen und die ``sensebox.ino`` Datei auswählen
* Im Dialogfeld wird gefragt, ob die Datei verschoben werden darf. Dieses mit "Ja" oder "Ok" bestätigen.
* Jetzt musst du dein WiFi-Netzwerk und dein Passwort für das Netzwerk zwischen die ``""`` eingeben. Achte darauf, keine Leerzeichen zwischen den ``"`` und den Buchstaben deines Passworts zu haben.  
* Jetzt kannst du das Programm über das Pfeil Icon auf den Mikrocontroller laden.
* Warten bis das Programm übertragen wurde
__________


### Ethernet-Bee

* Arduino Anwendung öffnen
* In der Menüleiste ``Datei`` → ``Öffnen`` auswählen und die ``sensebox.ino`` Datei auswählen
* Im Dialogfeld wird gefragt ob die Datei verschoben werden darf. Dieses mit "Ja" oder "Ok" bestätigen.
* Jetzt kannst du das Programm über das Pfeil Icon auf den Mikrocontroller laden.
* Warten bis das Programm übertragen wurde
___________________



### LoRa-Bee

* Arduino Anwendung öffnen
* In der Menüleiste ``Datei`` → ``Öffnen`` auswählen und die ``senseBox.ino`` Datei auswählen
* Im Dialogfeld wird gefragt ob die Datei verschoben werden darf. Dieses mit "Ja" oder "Ok" bestätigen.
* Jetzt kannst du das Programm über das Pfeil Icon auf den Mikrocontroller laden.
* Warten bis das Programm übertragen wurde
___________

Wenn alles richtig gelaufen ist, kannst du nun auf der openSenseMap deine Station auswählen und verfolgen, wie Messungen kontinuierlich übertragen werden!

<div class="box_info">
    <i class="fa fa-info fa-fw" aria-hidden="true" style="color: #42acf3;"></i>
  Du kannst dich nicht mehr daran erinnern, wie du den Code von Arduino auf die senseBox überträgst? Schau nochmal in <a href="../erste-schritte/software-installation.html">Schritt 1</a> und <a href="../erste-schritte/komponenten-testen.html">Schritt 4</a> nach, dort wird die Installation und die Übertragung der Tests erklärt. Falls du weitere Fragen hast, nutze unser <a href="https://forum.sensebox.de/">Forum</a>, um dich zu informieren oder gegebenenfalls einen eigenen Beitrag zu erstellen. </div>


