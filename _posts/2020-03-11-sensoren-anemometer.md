---
date: 2020-03-11
title: Anemometer
categories: hardware
description: senseBox Windsensor
type: Document
resources:
image1: /images/2020-03-11-sensoren-anemometer/anemometer-top.png
image2: /images/2020-03-11-sensoren-anemometer/anemometer-front.png

---

# senseBox Anemometer {#head}

Mit dem senseBox Anemometer kann die Windgeschwindigkeit gemessen werden

{% include image.html image=page.image1 %}
Ansicht von oben.

{% include image.html image=page.image2 %}
Ansicht von vorn.

Das Anemometer wird über einen JST-Stecker an einem der Analog/Digital-Ports der senseBox angeschlossen.

## Technische Details
- Typ: Gleichstrommotor
- Signalbereich: 0 bis maximal 1,2 V
- Messbereich: 0 bis ~28 m/s

### Maße
- Durchmesser Flügelrad: 60 mm
- Rotationsdurchmesser: 200 mm
- Flügelwinkel: 120°

## Programmierung (Arduino)
````
const unsigned int windspeedPin = 1; //Connected to Port: Digital A

void setup() {
  Serial.begin(9600);
}

void loop() {
  float voltage = analogRead(windspeedPin) * (3.3 / 1024.0);
  Serial.println(voltage);
  float windspeed = 0.0;
  if (voltage >= 0.018){
    float poly1 = pow(voltage, 3);
    poly1 = 17.0359801998299 * poly1;
    float poly2 = pow(voltage, 2);
    poly2 = 47.9908168343362 * poly2;
    float poly3 = 122.899677524413 * voltage;
    float poly4 = 0.657504127272728;
    windspeed = poly1 - poly2 + poly3 - poly4;
    //windspeed = windspeed * 0.2777777777777778; //conversion in m/s
  }
  Serial.println(windspeed);
  delay(50);
}
```


## Programmierung (Blockly)

Zur Zeit lässt sich das Anemometer noch nicht mit Blockly programmieren.