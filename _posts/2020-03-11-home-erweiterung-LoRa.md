---
date: 2020-03-11
title: senseBox:home mit LoRa
categories: sensebox-home
description: Daten der senseBox:home über LoRa verschicken
type: Document
set: sensebox-home-general
set_order: 3
image00: /images/2020-03-11-home-erweiterung-lora/home-lora-00.png
image01: /images/2020-03-11-home-erweiterung-lora/home-lora-01.png
image02: /images/2020-03-11-home-erweiterung-lora/home-lora-02.png
image03: /images/2020-03-11-home-erweiterung-lora/home-lora-03.png
image04: /images/2020-03-11-home-erweiterung-lora/home-lora-04.png
image05: /images/2020-03-11-home-erweiterung-lora/home-lora-05.png
image06: /images/2020-03-11-home-erweiterung-lora/home-lora-06.png
image07: /images/2020-03-11-home-erweiterung-lora/home-lora-07.png
image08: /images/2020-03-11-home-erweiterung-lora/home-lora-08.png
image09: /images/2020-03-11-home-erweiterung-lora/home-lora-09.png
image10: /images/2020-03-11-home-erweiterung-lora/home-lora-10.png
image11: /images/2020-03-11-home-erweiterung-lora/home-lora-11.png
image12: /images/2020-03-11-home-erweiterung-lora/home-lora-12.png
image13: /images/2020-03-11-home-erweiterung-lora/home-lora-13.png
image14: /images/2020-03-11-home-erweiterung-lora/home-lora-14.png
image15: /images/2020-03-11-home-erweiterung-lora/home-lora-15.png
image16: /images/2020-03-11-home-erweiterung-lora/home-lora-16.png
---

## LoRa und TheThingsNetwork

Die Daten werden über das [TheThingsNetwork](https://www.thethingsnetwork.org/) (TTN) versendet, daher muss im ersten Schritt dort ein Gerät angelegt und eine weiterleitung der Daten zur openSenseMap eingerichtet werden. 

## Registrieren im TheThingsNetwork

Viele Gateways, die von verschiedenen Gruppen, Vereinen oder auch Unternemhmen aufgestellt wurden, verwendet das TheThingsNetwork, um die Daten zu empfangen und zu versenden. Damit Daten innerhalb des Netzes empfangen und verabeitet werden können muss zuerst ein Account erstellt werden und die Geräte registriert werden.

Eine Übersicht über die Abdeckung findest du auf [ttnmapper.org](https://ttnmapper.org/). Beachte hierbei jedoch, dass die Abdeckung evlt. nicht der Realität entspricht.

### Anlegen

Erstelle dir einen neuen Account unter [https://www.thethingsnetwork.org/](https://www.thethingsnetwork.org/). Anschließe klicke auf Console und klicke auf Applications.

{% include image.html image=page.image00 %}

Du bekommst eine Übersicht über alle bereits registrierten **Applications** und kannst über **add Application** eine neue hinzufügen. 

{% include image.html image=page.image01 %}

Wähle einen Namen für deine Application und füge eine kurze Beschreibung hinzu. Alle anderen Parameter können unverändert bleiben.
{% include image.html image=page.image03 %}

Nach einem klick auf **Add Application** gelangst du auf die Übersichtsseite. 
{% include image.html image=page.image04 %}

Innerhalb einer Application können nun mehrere Devices registriert werden. Klicke dazu auf **Devices** und wähle **register Device**. 
{% include image.html image=page.image05 %}

Gib deinem **Device** eine einmale ID. Die Device EUI, der APP Key und auch die APP EUI werden später benötigt und automatisch generiert. 
{% include image.html image=page.image06 %}

### Anlegen der openSenseMap integration

Die Daten werden über das TheThingsNetwork als einfache Bytes versendet werden von dort an die openSenseMap weitergeleitet. Damit diese weiterleitung stattfinden kann klicke auf **Integrations** und lege anschließend eine neue Integration an. 

Für einige Dienste sind bereits vorgefertigte **Inteegrations** angelegt. Für die Weiterleitung an die openSenseMap verwenden wir die einfache **HTTP-Integration**. 

{% include image.html image=page.image07 %}

Gib der Integration einen Namen und trage ihn unter Process ID ein. Wähle als **Access Key** den __default key__ aus. Als URL für die Integration wird `https://ttn.opensensemap.org/v1.1`. Alle anderen Parameter können unverändert bleiben. 

{% include image.html image=page.image09 %}

Die Registrierung im TheThingsNetwork ist nun abgeschlossen. 


## Registrieren auf der openSenseMap

Die Registrierung auf der openSenseMap erfolgt wie hier beschrieben. Wähle unter Verbindsart LoRa aus und füge die Sensoren hinzu, die du im ersten Schritt an deine senseBox angeschlossen hast. 

Damit die Verbindung zwischen dem TheThingsNetwork und der openSenseMap korrekt erfolgt muss im nächsten Schritt noch **senseBox:home** als Dekodierungs-Profil ausgeäwhlt werden. Füge noch deine TTN Application-ID und deine TTN Device-ID ein. Klicke auf weiter, um die Registrierung abzuschließen.

## Kompilieren und übertragen

Nach der Registrierung kannst du deinen Programmcode für die senseBox direkt über die openSenseMap kompilieren. Du musst daher keine Software auf dem Computer installieren. 

{% include image.html image=page.image12 %}
{% include image.html image=page.image13 %}


Kopiere die Device EUI, die Application EUI und den Application Key aus der Device Übersicht in die entsprechenden Felder und drücke Kompilieren.

### Kopieren auf die senseBox

Bringe die senseBox durch einen doppelklick auf den roten Resetbutton in den Lernmodus. Die senseBox taucht nun als Wechseldatenträger auf und du kannst das zuvor heruntergeladene Programm auf die senseBox kopieren. Anschließend startet die senseBox automatisch neu und die Daten werden übertragen.

## Probleme

Sollten deine Daten nicht auf der openSenseMap angezeigt werden solltest du als erstes Überprüfen ob die Daten im TheThingsNetwork ankommen. Klicke dazu in deinem **Device Overview** auf Data und schaue ob dort Daten ankommen. Zum einen solltest du eine Aktivierungsnachricht sehen, die mit einem Blitz gekenntzeichnet ist. Die ankommenden Daten werden mit Payload gekennzeichnet.

{% include image.html image=page.image14 %}

Sollten Daten in der Console auftauchen diese allerdings nicht an die openSenseMap weitergeleitet werden überprüfe ob alle Parameter für die Integration von TTN auf der openSenseMap richtig kopiert worden sind. Die Paremter findes im Dasboard der openSenseMap.


{% include image.html image=page.image15 %}

Klicke auf bei deiner senseBox auf Editieren und wähle anschließend im Seitenmenü TheThingsNetwork aus. 

{% include image.html image=page.image16 %}

