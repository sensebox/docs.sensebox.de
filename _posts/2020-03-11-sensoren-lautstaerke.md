---
date: 2020-03-11
title: Umweltsensor
categories: sensoren
description: Luftdruck- und Temperatursensor (BME680)
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.kaufen/product/lautstarkesensor
  - name: DFRobot SEN0232 Gravity
    link: https://www.mouser.de/pdfdocs/SEN0232_Web.pdf
---
# Lautstärkesensor {#head}
Der DFRobot SEN0232 misst die Lautstärke und gibt die Messwerte in Dezibel aus.

![Der Geräuschpegel-Sensor](https://github.com/sensebox/resources/raw/master/gitbook_pictures/decibel_meter.jpg)

## Technische Informationen

* Maße: 60mm x 43mm x 9mm
* "Plug-in-and-Go" senseBox kompatibel
* Eingangsspannung: 3,3-5V
* Ausgangsspannung: 0,6-2,6V
* Messspanne: zwischen 30dBA und 130 dBA akkurat
* Messintervall: 125ms

![Anschluss des Sensors](https://github.com/sensebox/resources/raw/master/gitbook_pictures/SoundLevelMeter.png)


## Programmierung (Arduino)

Im ersten Code-Snippet wird lediglich die Eingangsspannung ausgelesen und in Dezibel konvertiert. Der Wert wird auf der Konsole in Arduino angezeigt.
Sind diese halbwegs nachvollziehbar - werden größer wenn man z.B. in der Nähe des Sensors klatscht und werden dementsprechend kleiner, wenn keine wahrnehmbare Geräuschkulisse vorliegt - dann ist der Sensor einsatzbereit.
```arduino
#define SoundSensorPin A1  //this pin read the analog voltage from the sound level meter
#define VREF  5.0  //voltage on AREF pin,default:operating voltage

void setup()
{
    Serial.begin(115200);
}

void loop()
{
    float voltageValue,dbValue;
    voltageValue = analogRead(SoundSensorPin) / 1024.0 * VREF;
    dbValue = voltageValue * 50.0;  //convert voltage to decibel value
    Serial.print(dbValue,1);
    Serial.println(" dBA");
    delay(125);
}
```

## Programmierung (Blockly)
