---
date: 2020-10-20
title: Das CO2-Ampel-Set
categories: hardware
description: Das CO2-Ampel-Set
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.kaufen/product/co2-ampel-bausatz
  - name: senseBox CO2 Ampel Programmcode V1
    link: /docs/sensebox_co2_ampel.bin
image1: /images/2020-10-22-sets-co2-ampel/image1.png
image2: /images/2020-10-22-sets-co2-ampel/image2.png
image3: /images/2020-10-22-sets-co2-ampel/image3.png
image4: /images/2020-10-22-sets-co2-ampel/image4.png
image5: /images/2020-10-22-sets-co2-ampel/image5.png
image6: /images/2020-10-22-sets-co2-ampel/image6.png
image7: /images/2020-10-22-sets-co2-ampel/image7.png
image8: /images/2020-10-22-sets-co2-ampel/image8.png
image9: /images/2020-10-22-sets-co2-ampel/image9.png
image10: /images/2020-10-22-sets-co2-ampel/image10.png
image11: /images/2020-10-22-sets-co2-ampel/image11.png
image12: /images/2020-10-22-sets-co2-ampel/image12.png
image13: /images/2020-10-22-sets-co2-ampel/image13.png
image14: /images/2020-10-22-sets-co2-ampel/image14.png
image15: /images/2020-10-22-sets-co2-ampel/image15.png
image16: /images/2020-10-22-sets-co2-ampel/image16.png
image17: /images/2020-10-22-sets-co2-ampel/image17.png
image18: /images/2020-10-22-sets-co2-ampel/image18.png
image19: /images/2020-10-22-sets-co2-ampel/image19.png
image20: /images/2020-10-22-sets-co2-ampel/image20.png
image21: /images/2020-10-22-sets-co2-ampel/image21.png
image22: /images/2020-10-22-sets-co2-ampel/image22.png
image23: /images/2020-10-22-sets-co2-ampel/image23.png
image24: /images/2020-10-22-sets-co2-ampel/image24.png
image25: /images/2020-10-22-sets-co2-ampel/image25.png
image26: /images/2020-10-22-sets-co2-ampel/image26.png

---


*vorläufige Version - vom 22.10.202*

{% include image.html image=page.image1 %}

# Benötigte Bauteile
{% include image.html image=page.image2 %}

-   senseBox Mikrocontroller (MCU) Lite
-   CO2 Sensor
-   RGB LED
-   Display
-   3x JST Verbindungskabel
-   Gehäuseteile
    -   6x Platten aus Plexiglas
    -   1x Stück Milchplexiglas
    -   11x Abstandshalter kurz
    -   4x Abstandshalter mittel
    -   4x Abstandshalter lang
    -   2x schwarze Plastikclips
    -   PCB Sensorhalterung
-   USB Kabel
-   USB Netzteil

# Aufbau

## 1.  Sensorhalterung vorbereiten

An die Sensorhalterung werden das Display, der CO2 Sensor und die RGB
LED angebracht. Später wird sie mit der Hauptplatine verbunden und
getestet.

Bringt als erstes auf der Oberseite die vier mittleren Abstandshalter
an:
{% include image.html image=page.image3 %}
>
> Als nächstes braucht ihr 6 kurze Abstandshalter und befestigt sie wie
> folgt auf der gleichen Seite der PCB-Halterung:\
> \
{% include image.html image=page.image4 %}

Nun 5 kurze Abstandshalter auf der Unterseite anbringen:

{% include image.html image=page.image5 %}
Auf die Unterseite werden jetzt der CO2 Sensor und die RGB LED eingehängt:

{% include image.html image=page.image6 %}
{% include image.html image=page.image7 %}
Auf die Oberseite als letztes das Milchplexiglas über der RGB LED anbringen und das Display an das andere Ende. Achtet beim Display auf die korrekte Orientierung:

{% include image.html image=page.image8 %}

Eurer Ergebnis sollte so aussehen:
{% include image.html image=page.image9 %}
{% include image.html image=page.image10 %}
## 2.  Komponenten mit MCU verbinden

Steckt die vier langen Abstandshalter in die Ecklöcher der senseBox MCU:

{% include image.html image=page.image11 %}

Bevor ihr die Platine an der Unterseite vom Gehäuse befestigt, entfernt
zuerst die Schutzfolie von beiden Seiten der großen Plexiglasplatte:

{% include image.html image=page.image12 %}

Jetzt die MCU so auf die Platte setzen, dass die Eckpunkte in die vier
Bohrlöcher passen und die Platine nicht die länglichen Einschnitte vom
Gehäuseboden verdecken:

{% include image.html image=page.image13 %}

Nutzt zur Befestigung die schwarzen Plastikclips. Steckt sie dazu von
unten durch die Plexiglasplatte und dann durch die Platine. Drückt sie
fest bis sie einrasten:

{% include image.html image=page.image14 %}
{% include image.html image=page.image15 %}

Steckt jetzt ein Verbindungskabel für die RGB LED in einen der digitalen
Anschlüsse und zwei Verbindungskabel für Display und CO2-Sensor in einen
der drei I2C Steckplätze:

{% include image.html image=page.image6 %}

Jetzt könnt ihr die Kabel an den CO2-Sensor, das Display und die RGB LED
Anschließen. Hierbei darauf achten, dass die RGB LED mit dem digitalen
Anschluss verbunden ist, bzw. das Display und der CO2-Sensor mit je
einem der I2C Anschlüsse:

{% include image.html image=page.image17 %}
{% include image.html image=page.image18 %}
Jetzt könnt ihr die Sensorhalterung mit der MCU über die langen
Abstandshalter verbinden. Achtet hierbei darauf, dass die Halterung
nicht falsch herum angebracht wird und sich genau parallel über die MCU
befindet:

{% include image.html image=page.image19 %}

## 3.  Software aufspielen und testen

Um die Ampel testen zu können müsst ihr [hier](/docs/sensebox_co2_ampel_v1.bin) Programmdatei runterladenund auf die senseBox
übertragen. Schließt dazu die Messstation mit dem USB Kabel an einen PC
an. Neben dem USB Anschluss auf der MCU befindet sich ein roter Knopf.
Drückt ihn zweimal hintereinander.

{% include image.html image=page.image20 %}

Daraufhin sollte in eurem Betriebssystem die senseBox als neuer
Wechseldatenträger erscheinen.

{% include image.html image=page.image21 %}

Kopiert jetzt die Datei *sensebox_co2_ampel.bin* aus eurem
Downloadordner auf den „SENSEBOX" Wechseldatenträger:

{% include image.html image=page.image22 %}

Die Station startet danach automatisch neu und sollte euch die ersten
Messwerte auf dem Display anzeigen.

{% include image.html image=page.image23 %}

Für den Fall dass das Display schwarz bleibt, drückt einmal auf den oben
genannten Resetknopf um das Programm auf der Station neu zu starten.

## 4.  senseBox ins Gehäuse einbauen

Als nächstes werden die Seitenwände eingesetzt. Entfernt hierbei NICHT
die Folie von den Seitenteilen entfernen, da sie dann beim
Zusammenstecken fester sitzen bleiben:
{% include image.html image=page.image25 %}

Als letztes vom Gehäusedeckel auf beiden Seiten die Schutzfolie
entfernen und ihn so anbringen, dass die Abstandshalter und die
Seitenteile einrasten:

{% include image.html image=page.image26 %}

Nun ist die CO2-Ampel einsatzbereit! Ihr könnt sie jetzt aufhängen und
über das USB Kabel und das Netzteil an eine Steckdose anschließen.

