---
date: 2020-03-11
title: Ultrasonic distance sensor
categories: hardware
description: HC-SR04
type: Document
resources:
image1: /images/2020-03-11-sensoren-distanz/US-Sensor.png
aufbau: /images/2020-03-11-sensoren-distanz/Aufbau-Ultraschall.png
block: /images/2020-03-11-sensoren-distanz/ultraschall-block-en.svg

---
The HC-SR04 measures distances using ultrasound and outputs them in centimeters (cm).

{% include image.html image=page.image1 %}


## Technical Information

* Dimensions: 45mm x 20mm x 17mm
* Supply voltage of 5V with a current consumption of less than 2mA
* up to 50 measurements per second possible


## Programming (Arduino)

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
## Programming (Blockly)

In Blockly the sensor can be read out via the following block:

{% include image.html image=page.block %}


Select the port where you have connected the sensor from the drop-down menu. Trigger and echo pin will be adjusted automatically.

