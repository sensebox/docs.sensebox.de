---
date: 2020-03-11
title: GPS
categories: sensoren
description: GPS u-blox CAM-M8Q Multi GNSS Modul
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.kaufen/product/gps
  - name: "CAM M8Q"
    link: https://sensebox.kaufen/assets/datenblatt/senseBox-CAM-M8Q_v20.pdf
---

Das GPS-Modul empfängt die Position (Längengrad/Breitengrad/Höhe) der senseBox. Diese kann für mobile Anwendungen, z.B. die mobile Datenübertragung auf die openSenseMap, genutzt werden. Dieser Sensor ist kompatibel mit den gängingen GNS Systemen (GPS, QZSS, GLONASS, BeiDou, Galileo) und basiert auf dem u-blox CAM-M8Q Multi GNSS Modul.

![Der GPS-Sensor](https://github.com/sensebox/resources/raw/master/gitbook_pictures/gps%20top.png)

Der GPS Sensor wird an einen I2C-Port angeschlossen.

## Technische Details
- "Plug-in-and-Go" senseBox kompatibel durch Breakout-Board mit JST-Anschluss
- Simultanempfang von GPS, QZSS, GLONASS, BeiDou
- Navigationsempfindlichkeit von –167 dBm
- Empfänger: 72-Kanal u-blox M8
- Update-Rate: Single GNSS - bis zu 18Hz, Dual GNSS bis zu 10Hz
- Stromaufnahme: 30mA im Dauerbetrieb bzw. 10mA Power Save Mode 1Hz bei 3V


## Programmierung 

```arduino
#include <senseBoxIO.h>
#include <TinyGPS++.h>
#include <SPI.h>
#include <Wire.h>

Wire.requestFrom(0x42,10);
while (Wire.available())
    gps.encode(Wire.read());
```


## Programmierung (Blockly)

In Blockly kann der Sensor über folgenden Block ausgelesen werden:



Im Block kannst du zwischen Luftdruck und Temperatur auswählen.