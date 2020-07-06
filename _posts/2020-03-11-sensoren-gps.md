---
date: 2020-03-11
title: GPS
categories: hardware
description: GPS u-blox CAM-M8Q Multi GNSS Modul
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.kaufen/product/gps
  - name: "CAM M8Q"
    link: https://sensebox.kaufen/assets/datenblatt/senseBox-CAM-M8Q_v20.pdf
image: /images/2020-03-11-sensoren-gps/gps.png    
block: /images/2020-03-11-sensoren-gps/block-gps-en.svg
---

The GPS module receives the position (longitude/latitude/altitude) of the senseBox. This can be used for mobile applications, e.g. mobile data transfer to the openSenseMap. This sensor is compatible with the most common GNS systems (GPS, QZSS, GLONASS, BeiDou, Galileo) and is based on the u-blox CAM-M8Q Multi GNSS module.

{% include image.html image=page.image %}

The GPS sensor is connected to an I2C port.

## Technical Details
- "Plug-in-and-Go" senseBox compatible through breakout board with JST connector
- Simultaneous reception of GPS, QZSS, GLONASS, BeiDou
- Navigation sensitivity of -167 dBm
- Receiver: 72-channel u-blox M8
- Update rate: Single GNSS - up to 18Hz, Dual GNSS up to 10Hz
- Current consumption: 30mA in continuous operation or 10mA Power Save Mode 1Hz at 3V


## Programming (Arduino)

```arduino
#include <SenseBoxMCU.h>

GPS gps;
float lat; //Geografische Breite
float lng; //Geografische Länge
float alt; //Höhe über Meeresspiegel in Metern
float speed;
float date;
float time;

void setup()
{
  gps.begin();
}

void loop()
{
  gps.getGPS();
  lat = gps.getLatitude();
  lng = gps.getLongitude();
  alt = gps.getAltitude();
  speed = gps.getSpeed();
  date = gps.getDate();
  time = gps.getTime();

  Serial.print(lat, 6);
  Serial.print(F(","));
  Serial.print(lng, 6);
  Serial.print(F(","));
  Serial.println(alt, 1);
  Serial.print(F(","));
  Serial.println(speed, 4);
  Serial.print(F(","));
  Serial.println(date);
  Serial.print(F(","));
  Serial.println(time);
  delay(100);
}
```


## Programming (Blockly)

In Blockly the sensor can be read out via the following block:

{% include image.html image=page.block %}

In the block you can choose between the different parameters of the GPS module:
- Longitude
- Latitude
- Height
- timestamp (RFC3339)
- Speed
- Date
- Time