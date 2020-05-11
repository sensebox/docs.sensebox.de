---
date: 2020-03-11
title: Ultraschall Distanzsensor
categories: sensoren
description: HC-SR04
type: Document
resources:
aufbau: /images/2020-03-11-sensoren-distanz/Aufbau-Ultraschall.png
block: /images/2020-03-11-sensoren-distanz/ultraschall-block.svg

---
Der HC-SR04 misst Distanzen mit Hilfe von Ultraschall und gibt diese in Zentimetern (cm) aus.

![Der Ultraschall Distanzsensor](https://sensebox.kaufen/api/public/uploads/1526397840835-Sonar_03.png)

## Technische Informationen

* Maße: 45mm x 20mm x 17mm
* Versorgungsspannung von 5V bei einer Stromaufnahme weniger als 2mA
*  bis zu 50 Messungen pro Sekunde möglich

{% include image.html image=page.aufbau %}


## Programmierung (Arduino)


```arduino
int trig = 1;  // Trig-Pin des Sensors ist an Pin 1 angeschlossen.
int echo = 2;  // Echo-Pin des Sensors ist an Pin 2 angeschlossen.

// Definieren der Variablen
unsigned int time = 0;
unsigned int distance = 0;

void setup() {
Serial.begin(9600); // Startet den Seriellen Monitor
pinMode(trig, OUTPUT);  
pinMode(echo, INPUT);
}

void loop() {
digitalWrite(trig, HIGH);
delayMicroseconds(10);
digitalWrite(trig, LOW);
distance = time / 58;
Serial.println(distance);
}
```
## Programmierung (Blockly)

In Blockly kann der Sensor über folgenden Block ausgelesen werden:

{% include image.html image=page.block %}


Wähle den Port, an dem du den Sensor angeschlossen hast über das Dropdown-Menü aus. Trigger und Echo Pin werden dann automatisch angepasst.


