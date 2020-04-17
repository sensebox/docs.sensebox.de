---
date: 2020-03-11
title: Umweltsensor
categories: sensoren
description: Luftdruck- und Temperatursensor (BME680)
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.kaufen/product/sensebox-mini
  - name: Bosh BME680
    link: https://www.bosch-sensortec.com/media/boschsensortec/downloads/datasheets/bst-bme680-ds001.pdf
---

Mit dem Sensor BME680 kannst du eine verschiedene Auswahl an Phänomenen messen. Lufttemperatur, relative Luftfeuchtigkeit, Luftdruck und Luftqualität können mit dem BME680 bestimmt werden. Er ist also ein echter Alleskönner. 

![Der BME680](https://github.com/sensebox/resources/raw/master/gitbook_pictures/bme.png)

## Technische Details
* Schnelle Reaktionszeit von weniger als 10 Sekunden
* "Plug-in-and-Go" senseBox kompatibel
* Abweichung bei Gasmessungen von +-15%

## Anschluss und Programmierung

Mit dem mitgelieferten Verbindungskabel kannst du deinen Gassensor mit dem "I2C"-Port der senseBoxMCU verbinden. 
Ist dies erledigt können wir nun im Programmcode den Sensor initialisieren und uns die ersten Messwerte ausgeben lassen.

**Achtung**Der BME Gassensor ist nicht mit dem BMP280 Luftdrucksensor kompatibel. Das heißt du kannst nur einen der beiden gleichzeitig anschließen und auslesen!



Als erstes muss die Bibliothek geladen und eine Instanz des Sensors erstellt werden.

```arduino 
#include <SenseBoxMCU.h>

BME680_Class BME680;

void setup(){
    // Normalen seriellen Port initialisieren 
    Serial.begin(9600);
    while(!Serial);

    // Starten des Sensors
    BME680.begin(I2C_STANDARD_MODE);
    delay(2000);

    // Oversampling der Sensoren festlegen
    BME680.setOversampling(TemperatureSensor, Oversample16);
    BME680.setOversampling(HumiditySensor, Oversample16);
    BME680.setOversampling(PressureSensor, Oversample16);
    Serial.println(F("- Setting IIR filter to a value of 4 samples"));
    // IIR Filter auf 4 Werte setzen
    BME680.setIIRFilter(IIR4);
    BME680.setGas(320, 150);
}

void loop(){
    // Variable um Messwerte zu speichern
    static int32_t temperature, humidity, pressure, gas;

    // Aktuelle Messwerte auslesen und speichern
    BME680.getSensorData(temperature, humidity, pressure, gas); 
    
    // rel. Luftfeuchte in milli-prozent
    Serial.print(humidity / 1000.0, 2);                      
    Serial.print(F("%rel. Luftfeuchte "));
    
    // Luftdruck in Hectopascals
    Serial.print(pressure / 100.0, 2);                       
    Serial.print(F("hPa "));

    // Luftqualität in mOhm
    Serial.print(gas / 100.0, 2);                            
    Serial.println(F("mOhm"));
    delay(5000);
}
```

