---
date: 2020-03-11
title: 'Schritt 1: Aufbau der Hardware'
title_order: 1
categories: aufbau-sensebox-home
description: Schritt 1 zum Aufbau der senseBox:home.
type: Document
set: aufbau-sensebox-home
set_order: 1
next: /sdjklsdf/
image1: /images/sensebox-home/sensebox-home-1.jpg
image2: /images/sensebox-home/sensebox-home-2.jpg
image3: /images/sensebox-home/sensebox-home-3.jpg
image4: /images/sensebox-home/sensebox-home-4.jpg
image5: /images/sensebox-home/sensebox-home-5.jpg
image6: /images/sensebox-home/sensebox-home-7.jpg
image6: /images/sensebox-home/sensebox-home-10.jpg
image7: /images/sensebox-home/sensebox-home-11.jpg
image8: /images/sensebox-home/sensebox-home-13.jpg
image9: /images/sensebox-home/sensebox-home-14.jpg
image10: /images/sensebox-home/sensebox-home-15.jpg
image11: /images/sensebox-home/sensebox-home-16.jpg
image12: /images/sensebox-home/sensebox-home-17.jpg
image13: /images/sensebox-home/sensebox-home-19.jpg
image14: /images/sensebox-home/sensebox-home-20.jpg
image15: /images/sensebox-home/sensebox-home-22.jpg
image16: /images/sensebox-home/sensebox-home-23.jpg
image17: /images/sensebox-home/sensebox-home-24.jpg
image18: /images/sensebox-home/sensebox-home-25.jpg
image19: /images/sensebox-home/sensebox-home-26.jpg
image20: /images/sensebox-home/sensebox-home-27.jpg
image21: /images/sensebox-home/sensebox-home-28.jpg
image22: /images/sensebox-home/sensebox-home-29.jpg
image23: /images/sensebox-home/sensebox-home-30.jpg
---


## Willkommen zum Tutorial für den Zusammenbau der senseBox:home

Da die senseBox ein modularer Bausatz ist, können einzelne Schritte zu Sensoren abweichen oder sogar in deinem Fall übersprungen werden. Zuerst zeigen wir Euch, wie der Microcontroller in das Gehäuse eingesetzt wird.
{% include image.html image=page.image1 %}
Dazu nehmt ihr das Gehäuse und richtet es mit der Aufbohrung nach unten aus. Der grüne senseBox Microcontroller wird nun auf der gegenüberliegenden Seite aufgelegt, sodass der rote Reset Knopf und der USB-Port nach vorne zeigen. 



{% include image.html image=page.image2 %}

Nun nehmt ihr die zwei beiliegenden kleineren Schrauben und befestigt die Platine über die mittleren Bohrlöcher am Gehäuse. Wenn die Platine etwas Spielraum hat ist das kein Problem. 

## Aufsetzten des WiFi-Bee
Als nächstes zeigen wir, wie das Wifi-Bee aufgesetzt wird. 

Dazu haben wir auf alle Bees eine Kennzeichnung aufgedruckt, welche die Richtung anzeigt. Wenn du ein anderes Datenübertragungsmodul hast, z.B. LAN, oder LoRaWAN, erfolgt das aufsetzten aber genau gleich. 
{% include image.html image=page.image3 %}

Das Wifi-Bee wird auf den XBee-Port 1 aufgesetzt und vorsichtig in die Sockelleiste eingedrückt, sodass alle Pins des Bees eingesteckt sind.

{% include image.html image=page.image4 %}


## Aufbau des Strahlenschutz-Gehäuse

Nun zeigen wir den Aufbau des Stahlenschutz-Gehäuses in welchem der Temperatur und Luftfeuchtigkeitssensor angebracht wird.
Im Strahlenschutz befinden sich einige Befestigungsteile um diesen später außen anzubringen. Diese brauchen wir erstmal nicht. 

{% include image.html image=page.image5 %}

Zuerst wird ein langes senseBox Kabel durch die Öffnung im Bodes des Strahlenschutzes gezogen und der Temperatur- und Luftfeuchtigkeitssensor Innen angesteckt.

{% include image.html image=page.image6 %}

Der Sensor kann nun zusätzlich noch mit etwas Klebeband oder einem Kabelbinder am Ständer befestigt werden. Das Strahlenschutzgehäuse sorgt später für eine gute Luftzirkulation und schützt den Sensor gleichzeitig vor der Witterung.
02:34 Nun kann das Strahlenschutzgehäuse noch zusammengesteckt werden und später wird der Sensor dann mit der senseBox Microcontroller verbunden.

## Aufbau des Feinstaubsensors


Als nächstes zeigen wir den Aufbau des Feinstaub-Sensors. 
{% include image.html image=page.image7 %}


{% include image.html image=page.image8 %}
Dazu muss das Gehäuse für den Sensor mit Öffnungen für Kabel und die Luftzufuhr versehen werden. 
Die Öffnungen sollen gegenüberliegend auf den Seiten mit jeweils zwei Sollbruchstellen liegen. 
Aus Sicherheitsgründen empfehlen wir die Öffnungen aufzubohren. Theoretisch, kann man die Öffnungen aber auch an den Sollbruchstellen mit einem stumpfen Gegenstand aufschlagen.  


Als nächstes nehmen wir den Feinstaubsensor und legen ihn in das Gehäuse, sodass der Kabel-Anschluss und der Luftansaugstutzen an den gerade gebohrten Öffnungen liegen.

{% include image.html image=page.image9 %} 

Das Kabel für den Feinstaubsensor hat eine andere Farbe und wird mit dem größeren Anschluss am Sensor angebracht. 


Dann werden die Verschraubungen für den Kabelanschluss angebracht.
Einfach die Kabelverschraubung auseinander schrauben und dann die einzelnen Teile in der richtige Reihenfolge einsortieren. Dann noch schnell zusammenschrauben und das wars.

{% include image.html image=page.image10 %} 
 Auf der anderen Seite des Sensors wird nun der Schlauch auf den Luftansaugstutzen aufgesteckt.
Hier benutzen wir auch eine Kabelverschraubung um den Schlauch abzudichten. Dann heißt es wieder alles richtig einsortieren. Am Ende ist etwas Druck auf den Schlauch nötig um Ihn auf den Stutzen aufzusetzen. Als letztes noch den Deckel aufsetzen und der Feinstaubsensor ist fertig.

{% include image.html image=page.image11 %} 
## Anschluss der externen Sensoren an die MCU

{% include image.html image=page.image12 %} 
Die außenliegenden Sensoren, also der Sensor für Temp. Und Luftfeuchtigkeit, sowie der Feinstaubsensor werden jetzt an die MCU angeschlossen.
Dafür nehmen wir zuerst das Kabel aus dem Strahlenschutz und fädeln es durch die letzte Kabelverschraubung in das Gehäuse.
{% include image.html image=page.image13 %} 
Dort wird das Kabel in einen der Steckplätze mit der Aufschrift I2C/Wire eingesteckt. 
{% include image.html image=page.image14 %} 


Danach wird das Kabel aus dem Feinstaubsensor genommen und durch die Verschraubung eingefädelt. 
Dieses Kabel kommt in einen der Steckplätze welche mit UART/Serial beschriftet sind. 

{% include image.html image=page.image15 %} 

## Verbinden des USB Kabels

{% include image.html image=page.image16 %} 

Als letztes schließen wir noch das Mini-USB Kabel an, über welches der Micro Controller programmiert wird, sowie die senseBox später im Betrieb mit Strom versorgt wird. 
Bitte beachte, dass der Mini-USB Port empfindlich ist und außerdem der Hebelwirkung des Kabels ausgesetzt ist. Deshalb sollte später möglichst nicht am USB-Kabel gerissen werden.
{% include image.html image=page.image17 %} 

## Anschluss der internen Sensoren an die MCU

{% include image.html image=page.image18 %} 
Nachdem die äußeren Sensoren angeschlossen sind, werden die übrigen Sensoren im Gehäuse angebracht.
Dafür wird eine Montageebene aufgebaut. Zuerst werden vier Abstandhalter in die außenliegenden Löcher des Mikrocontrollers eingesteckt. 
Die Abstandshalter haben einen Rastermechanismus. Deshalb sollten diese, falls Sie mal gelöst werden müssen, nicht mit Gewalt rausgerissen werden, sondern leicht am Kopf eingedrückt werden.  
Danach schließen wir zwei senseBox Kabel in die I2C/Wire Steckplätze um dort den Luftdruck Sensor und den Lichtsensor anzubringen.
{% include image.html image=page.image19 %} 

Die Kabel werden durch die mittleren Aussparungen der Montageplatte gefädelt. 
{% include image.html image=page.image20 %} 
Dann wird die Montageplatte auf die Abstandshalter gedrückt und die Kabel mit den Sensoren verbunden. 
Die Sensoren mit jeweils zwei Abstandhalter ausgestattet und auf der Montageplatte befestigt. 
Hast du einen Lichtsensor gewählt, sollte dieser möglichst mittig im Gehäuse angebracht werden, um gute Messwerte zu erhalten.
Der Luftdruck-Sensor kann in den äußeren Steckplatz.
{% include image.html image=page.image21 %} 

Als letztes wird der Deckel mit den Schrauben versehen und ein Silikagelbeutel zum weiteren Schutz vor entstehende Feuchtigkeit in das Gehäuse gelegt.
{% include image.html image=page.image22 %} 
{% include image.html image=page.image23 %} 
Nun werden noch die Schnellverschlussschrauben eingedreht und damit die senseBox verschlossen. 
Ich hoffe du hattest Spaß beim Zusammenbau. Nun musst du nur noch deinen Code auf die senseBox laden und diese auf der openSenseMap registrieren. Weitere Informationen zum Aufbau der senseBox findest du auf sensebox.de/go oder im senseBox Forum. Vielen Dank das du dir das Video angeschaut hast und willkommen in der senseBox Community. 

<hr>
<a href="/aufbau-sensebox-home/home-schritt-2/" class="button" style="float: right;">Weiter mit Schritt 2</a>