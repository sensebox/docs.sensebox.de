---
date: 2020-04-07
title: Web
title_order: 5
categories: Blockly
description: Erste Schritte Web
type: Document
set: blockly-erste-schritte
set_order: 5
resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-04-08-blockly-web/blockly-Web-Wifi-1.svg
image2: /images/2020-04-08-blockly-web/blockly-Web-Wifi-2.svg
image3: /images/2020-04-08-blockly-web/blockly-Web-oSeM-1.svg
image4: /images/2020-04-08-blockly-web/blockly-Web-oSeM-2.svg
image5: /images/2020-04-08-blockly-web/blockly-Web-Telegram-1.svg
image6: /images/2020-04-08-blockly-web/blockly-Web-Telegram-2.svg
image7: /images/2020-04-08-blockly-web/blockly-Web-Telegram-3.svg
image8: /images/2020-04-08-blockly-web/blockly-Web-Telegram-4.svg
image9: /images/2020-04-08-blockly-web/blockly-Web-Web-1.svg
image10: /images/2020-04-08-blockly-web/blockly-Web-Web-2.svg
image11: /images/2020-04-08-blockly-web/blockly-Web-Web-3.svg
image12: /images/2020-04-08-blockly-web/blockly-Web-Web-4.svg
image13: /images/2020-04-08-blockly-web/blockly-Web-Web-5.svg
image14: /images/2020-04-08-blockly-web/blockly-Web-Web-6.svg
image15: /images/2020-04-08-blockly-web/blockly-Web-Web-7.svg
image16: /images/2020-04-08-blockly-web/blockly-Web-Web-8.svg
image17: /images/2020-04-08-blockly-web/blockly-Web-Web-9.svg
image18: /images/2020-04-08-blockly-web/blockly-Web-Web-10.svg
image19: /images/2020-04-08-blockly-web/blockly-Web-Web-11.svg
image20: /images/2020-04-08-blockly-web/blockly-Web-Web-12.svg
---

## Allgemeines
In Blockly hast du die verschieden Möglichkeiten Projekte umzusetzen, die mit dem Internet arbeiten.

## WiFi
Mit dem `Verbinde mit WLAN`-Block kannst du deine senseBox im Setup() mit einem WLAN-Netzwerk verbinden. Unter SSID muss der Netzwerkname und unter Passwort das WLAN-Zugangspasswort eingegeben werden.

{% include image.html image=page.image1 %}
<br>
Mit dem `Initialisiere WLAN Access Point`-Block kann deine senseBox ein WLAN-Netzwerk erstelle, in welches du mit anderen Geräten beitreten kannst. Um Textfeld SSID kannst du den Names deines Netzwerks festlegen.

{% include image.html image=page.image2 %}

## openSenseMap
Die [openSenseMap](https://www.opensensemap.org) ist ein freies Datenportal für Umweltdaten. Um Messwerte an diese senden zu können musst du zunächst eine neue senseBox anlegen. Im Anschluss daran werden dir eine Box ID und Sensor IDs für jeden angegebenen Sensor angezeigt. Mehr dazu findest du im Bereich zur openSenseMap.

Um Messwerte an die openSenseMap senden zu können, muss du deine Box zuerst mit ihr verbinden. Nutze dazu den `Verbinde mit openSenseMap`-Block. 

{% include image.html image=page.image3 %}
<br>
Im ersten Dropdown Menü des Blocks kannst du auswählen ob deine senseBox an die herkömmlichen openSenseMap oder an workshop.openSenseMap senden soll.

> **opensensemap.org:** senseBoxen, die für langfristige Messreihen angelegt wurden 
> 
> **workshop.opensensemap.org:** senseBoxen, die im Rahmen von kurzen Experimenten oder zum Testen angelegt wurden.

Im zweiten Dropdown-Menü des Block musst du auswählen, ob es sich bei deiner senseBox um eine stationäre oder eine mobile Station handelt und im Textfeld "senseBox ID" die, nach der Registrierung angezeigte, senseBox ID eintragen.
Im freien Blockabschnitt `Sensoren` müssen dann die angeschlossenen Sensoren mit Hilfe des `Sende Messwert an die openSenseMap`-Blocks angeknüpft werden.

{% include image.html image=page.image4 %}
<br>
In diesem Block muss unter "Sensor ID" die ebenfalls nach der Registrierung angezeigte Sensor-ID angefügt werden und an den freien Bockabschnitt der jeweilige Sensor.

> **Achtung:** Die Sensor-IDs sind sensorspezifisch. Es ist also wichtig darauf zu achten, welche ID welchem Sensor/Messwert zugeordnet ist.

## Webserver
Die senseBox kann als Webserver eingesetzt werden.

<table style="border-collapse:collapse;border-spacing:0" class="tg"><tr><th style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:middle;word-break:normal">Block</th><th style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:middle;word-break:normal">Funktion</th></tr><tr><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">{% include image.html image=page.image9 %}</td><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">Verwende diesen Block im Setup() um den HTTP-Server zu,initialisieren. Über das Feld Port kannst du einstellen über welchen,Port der Server im Broswer erreichbar sein soll. Standardmäßig ist hier,Port 80 eingetragen.</td></tr><tr><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">{% include image.html image=page.image10 %}</td><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">Dieser Block wird in der Endlosschleife verbunden. In den freien,Blockabschnitt fügst du die Blöcke ein, die ausgeführt werden sollen,,wenn eine Client (z.B. ein Nutzer über den Browser) auf den den Server,zugreift.</td></tr><tr><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">{% include image.html image=page.image11 %}</td><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">Dieser Block gibt dir die IP-Adresse deiner senseBox im Netzwerk zurück.</td></tr><tr><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">{% include image.html image=page.image12 %}</td><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">Dieser Block gibt dir die Methode zurück.</td></tr><tr><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">{% include image.html image=page.image13 %}</td><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">Dieser Block gibt dir die URI zurück.</td></tr><tr><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">{% include image.html image=page.image14 %}</td><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">Dieser Block gibt dir die HTTP Version zurüc.</td></tr><tr><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">{% include image.html image=page.image15 %}</td><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">Mit diesem Block kannst du einen HTTP Antwort an den Clienten senden,,wenn dieser auf den Server zugreift. Die Antwort ist der HTML Code, der,aus verschiedenen Blöcken zusammengebaut werden kann.</td></tr><tr><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">{% include image.html image=page.image16 %}</td><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">Mit diesem Block kannst du einen HTTP Antwort an den Clienten senden,,wenn dieser auf den Server zugreift. Die Antwort ist der HTML Code, der,aus verschiedenen Blöcken zusammengebaut werden kann.</td></tr><tr><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">{% include image.html image=page.image17 %}</td><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">Dieser Block kannst als Mögliche HTTP Antwort gesendet werden, wenn eine fehlerhafte Seite aufgerufen wird.</td></tr><tr><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">{% include image.html image=page.image18 %}</td><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">Dies ist der Grundbaustein für den HTML Code. An den Body hängst du deinen HTML Code, der den Aufbau der Website beschreibt.</td></tr><tr><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">{% include image.html image=page.image19 %}</td><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">Mit den Tags kannst du deine HTML-Seite direkt über Blockly aufbauen.</td></tr><tr><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">{% include image.html image=page.image20 %}</td><td style="border-color:#50af47;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 20px;text-align:left;vertical-align:top;word-break:normal">Diesen Block kannst du an den Grundbaustein für den HTML Code anhängen und eine .html Datei von SD-Karte laden</td></tr></table>

## LoRa

### Aktivierung

### Lora Message

### Cayenne LPP

## Telegram
Mit [Telegram](https://www.telegram.org) kannst du einen Chatbot bauen, der dir Hiflt deine senseBox von überall per Textnachricht auszulesen. 

> Telegram ist ein kostenloser Messenger, der die Möglichkeit bietet auf einfachste Art Chatbots anzulegen. Um diesen nutzen zu können benötigst du einen Telegram Account. Bei der Erstellung deines Chatborts wird die dann ein Token angezeigt, welches du in Blockly verwenden kannst um dich zu authentifizieren. Mehr zur Erstellung eines Chatbots findest du im Projekt [Telegram Chatbot für die senseBox mit Blockly](https://sensebox.de/projects/de/2019-12-15-telegram-blockly).

Mit dem `Telegram Bot initialisieren`-Block wird im Setup() die senseBox darauf vorbereitet Daten auf Anfrage an den Chatbot zu senden. Im Textfeld "Token" musst du den beim Erstellen deines Chatbots angezeigten Token eintragen.

{% include image.html image=page.image5 %}

Anschließend kann mit dem Block `Telegram mache` in der Endlosschleife() programmiert werden, was genau der Chatbot ausführen soll.

{% include image.html image=page.image6 %}

Die Blöcke `Bei Nachricht` und `Sende Nachricht` können im freien Blockabschnitt des `Telegam mache`-Blocks platziert werden um festzulegen was die senseBox beim Empfang einer bestimmten Nachricht ausführen soll.

<table style="border-collapse:collapse;border-spacing:0;border:none" class="tg"><tr><th style="font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;text-align:left;vertical-align:middle">{% include image.html image=page.image7 %}</th><th style="font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;text-align:left;vertical-align:top">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</th><th style="font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;text-align:left;vertical-align:top">{% include image.html image=page.image8 %}</th></tr></table>

Mit dem `Bei Nachricht`-Block kann eine Aktion festgelegt werden, die die senseBox ausführen soll wenn eine bestimmte Nachricht über Telegram eintrifft. Zum Beispiel eine LED an- oder ausschalten.

Mit dem `Sende Nachricht`-Block kann eine Nachricht über Telegram an den Nutzer des Bots gesendet werden.