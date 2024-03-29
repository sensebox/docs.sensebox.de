---
date: 2020-03-11
title: Registrieren einer neuen senseBox
categories: opensensemap
description: Registrieren einer neuen senseBox auf der openSenseMap
type: Document
---

Um eine neue senseBox auf der openSenseMap zu registrieren, muss zunächst unter *Anmelden* ein Nutzer-Account erstellt werden.
Anschließend ist unter dem User-Logo oben rechts das Dashboard zu finden, über welches senseBoxen hinzugefügt und [verwaltet](/opensensemap/opensensemap-manage/) werden können.

Unter *Neue senseBox* kann nun eine neue senseBox registriert werden. Die folgenden Angaben sind notwendig:

- **Name der senseBox**: z.B. der Standort
- **Aufstellungsort**: dient der Filterung von Boxen
- **Standort**: kann über die Karte ausgewählt werden
- **Modell**: bestimmt die Sensorkonfiguration

Es gibt eine Vorauswahl für verschiedene Modelle.
Falls eine nicht vorhandene Sensorkonfiguration vorliegt, können einzelne Sensoren unter *Manuelle Konfiguration* von Hand hinzugefügt werden.

Nachdem die Registrierung abgeschlossen wurde, wird ein Arduino-Sketch angezeigt, welcher die angegebenen Sensoren ausliest und deren Daten regelmäßig zur openSenseMap überträgt.
Um diesen auf die senseBox zu übertragen, wird die [Arduino IDE](https://www.arduino.cc/en/Main/Software) benötigt, eine exemplarische Installations-Anleitung für die *senseBox:home* ist [hier](https://home.books.sensebox.de/de/software_installation.html) zu finden.

## Erweiterte Konfiguration
Es besteht die Möglichkeit neben der [HTTP REST API](https://docs.opensensemap.org/) auch andere Schnittstellen zur Datenübertragung zu nutzen.
Einstellungen hierfür müssen unter dem entsprechenden Reiter im Abschnitt *Erweitert* vorgenommen werden.
Detaillierte Anleitungen dazu sind hier zu finden:

- [MQTT](mqtt_client.md)
- [TheThingsNetwork](ttn_integration.md)
