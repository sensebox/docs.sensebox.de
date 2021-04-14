---
date: 2021-01-28
title: Programmieren mit Circuit Python
categories: misc
description: Programmiere deine senseBox MCU mit Python
type: Document
resources:
  - name: "Circuit Python"
    link: https://circuitpython.org/board/sensebox_mcu/
  - name: "Bibliotheken"
    link: "https://circuitpython.org/libraries"
image1: /images/2021-01-28-rtc-modul/rtc.png
---

CircuitPython ist eine Programmiersprache, die das Experimentieren und Programmieren auf einfachen Mikrocontroller-Boards vereinfacht. Sobald das Board eingerichtet ist, kann mit einem beliebigen Texteditor programmiert werden. Die senseBox MCU ist CircuitPython kompatibel.

## Installation von Circuit Python

Die aktuellste Version kann immer über die offizielle [CircuitPython Website](https://circuitpython.org/board/sensebox_mcu/){:target="_blank"} heruntergeladen werden. 
Schließe die senseBox MCU mit einem USB Kabel an deinen Computer an und versetzte diese über einen Doppelklick auf den roten Reset-Button in den Programmiermodus. Kopiere die .uf2 Datei auf deine senseBox MCU. Anschließend wird die senseBox als neues Gerät mit den Namen "CircuitPy" erkannt.

## Programmieren

Öffne/erstelle die Datei Code.py auf dem Laufwerk "CircuitPy" und kopiere folgenden Code als erstes Beispiel:

```python
import board
import digitalio
import time
 
led = digitalio.DigitalInOut(board.GREEN_LED)
led.direction = digitalio.Direction.OUTPUT
 
while True:
    led.value = True
    time.sleep(0.5)
    led.value = False
    time.sleep(0.5)
    
```    

Nach dem Speichern der Datei wird der Code direkt ausgeführt und die kleine LED neben dem Resetbutton fängt an zu blinken. Du kannst nun den Code einfach verändern und speichern und dieser wird direkt ausgeführt.

Als Alternative kann auch folgender Web Editor verwendet werden:
https://sensebox-circuitpython-webide.netlify.app/


Viele weitere Informationen zur Programmierung mit CircuitPython sind über die offizielle [CircuitPython Website](https://circuitpython.org/awesome){:target="_blank"} erhältlich.

## Bibliotheken
Für die meisten Komponenten der senseBox stehen Bibliotheken bereit, die verwendet werden können. Hierbei ist allerdings zu beachten, dass die Bibliotheken auf das CIRCUITPY Laufwerk kopiert werden müssen. Insgesamt stehen hierfür 48Kb Speicher zur Verfügung. Das gesamte Paket mit den Bibliotheken kann [hier](https://circuitpython.org/libraries){:target="_blank"} heruntergeladen werden. Achtet darauf die *.mpy Version* herunterzuladen. 

## Serieller Monitor
Um auf den Seriellen Monitor zugreifen zu können über das Terminal 
```
ls /dev/tty.*
```
alle verfügbaren Ports auflisten lassen. Die senseBox MCU sollte als usbmodemXXX auftauchen.
```
screen /dev/tty.board_name 115200
```

## SD-Karte
Um Bibliotheken von SD Karte zu laden, folgenden Code als `sdmount_lib.py` auf die SD Karte kopieren.

```python
import sys
 
import adafruit_sdcard
import board
import busio
import digitalio
import storage
from digitalio import DigitalInOut, Direction 

xb2_pwr = DigitalInOut(board.XB2_PWR)
xb2_pwr.direction = Direction.OUTPUT
xb2_pwr.value = False


# Connect to the card and mount the filesystem.
spi = busio.SPI(board.SCK, board.MOSI, board.MISO)
cs = digitalio.DigitalInOut(board.XB2_CS)
sdcard = adafruit_sdcard.SDCard(spi, cs)
vfs = storage.VfsFat(sdcard)
storage.mount(vfs, "/sd")
sys.path.append("/sd")
sys.path.append("/sd/lib")
```

Die Bibliotheken können anschließend auf die SD Karte in /lib kopiert werden. 
Über `import sdmount_lib` wird das SD Modul aktiviert und die Libraries können verwendet werden.

https://learn.adafruit.com/adafruit-micro-sd-breakout-board-card-tutorial/circuitpython

## Deinstallation
Um Circuit Python zu deinstallieren, bringe die senseBox durch einen Doppelklick auf den roten Reset-Button in Programmiermodus. Kopiere einfach eine .bin Datei (z.B. in Blockly erstellt) auf die sensebox MCU und die senseBox MCU ist wieder wie gewohnt über Blockly und Arduino programmierbar.

## Stromversorgung der Anschlüsse
Per Default sind die einzelen Pins nicht mit Strom versorgt. Über folgenden Code (wie auch im SD-Beispiel verwendet) können die einzelen Schnittstellen mit Strom versorgt werden. Beachtet, dass die XB-Ports inverted sind.

* XB1_PWR = False //inverted
* XB2_PWR = False //inverted
* I2C_PWR = True
* UART_PWR = True

```
xb2_pwr = DigitalInOut(board.XB2_PWR)
xb2_pwr.direction = Direction.OUTPUT
xb2_pwr.value = True
```

