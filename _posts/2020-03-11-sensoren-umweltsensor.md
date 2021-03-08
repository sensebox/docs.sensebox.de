---
date: 2020-03-11
title: Umweltsensor
categories: hardware
description: Luftdruck- und Temperatursensor (BME680)
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.kaufen/product/sensebox-mini
  - name: Bosh BME680
    link: https://www.bosch-sensortec.com/media/boschsensortec/downloads/datasheets/bst-bme680-ds001.pdf
image: /images/2020-03-11-sensoren-umweltsensor/bme.png
block: /images/2020-03-11-sensoren-umweltsensor/block_umweltsensor.svg
---

Mit dem Sensor BME680 kannst du eine verschiedene Auswahl an Phänomenen messen. Lufttemperatur, relative Luftfeuchtigkeit, Luftdruck und Luftqualität können mit dem BME680 bestimmt werden. Er ist also ein echter Alleskönner. 

{% include image.html image=page.image %}

## Technische Details
* Schnelle Reaktionszeit von weniger als 10 Sekunden
* "Plug-in-and-Go" senseBox kompatibel
* Abweichung bei Gasmessungen von +-15%

## Anschluss und Programmierung

Mit dem mitgelieferten Verbindungskabel kannst du deinen Gassensor mit dem "I2C"-Port der senseBoxMCU verbinden. 
Ist dies erledigt, können wir nun im Programmcode den Sensor initialisieren und uns die ersten Messwerte ausgeben lassen.

**Achtung** Der BME Gassensor ist nicht mit dem BMP280 Luftdrucksensor kompatibel. Das heißt du kannst nur einen der beiden gleichzeitig anschließen und auslesen!


## Programmierung (Blockly)

In Blockly kann der Sensor über folgenden Block ausgelesen werden:

{% include image.html image=page.block %}

Im Block kannst du zwischen den verschiedenen Parametern des Umweltsensors auswählen:

- Temperatur in Grad Celsius (°C)
- Luftfeuchtigkeit in %
- Luftdruck in Pa
- Innenraumluftqualität (IAQ)
- Kalibrierungswert
- CO<sub>2</sub> Äquivalent
- Atemluft VOC Äquivalent

## Kalibrierungswert

Den Status der Kalibrierung kann über den Wert IAQ Accuracy abgelesen werden. Er ist entweder 0, 1, 2 oder 3 und sagt folgendes aus:

- IAQ Accuracy = 0 heißt Sensor wird stabilisiert (dauert ca. 25 Minuten) oder dass es eine Zeitüberschreitung gab (which should be indicated by a warning/error flag by BSEC ← Muss in Blockly abgefangen werden),
- IAQ Accuracy = 1 heißt Wert ist ungenau,
- IAQ Accuracy = 2 heißt Sensor wird kalibriert,
- IAQ Accuracy = 3 heißt Sensor erfolgreich kalibriert.

Der IAQ Index ist also nur aussagekräftig bei IAQ Accuracy = 3. Neben dem Wert für IAQ stellt uns BSEC noch K und VOC äquivalente Werte bereit. 
