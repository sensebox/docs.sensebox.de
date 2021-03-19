---
date: 2020-10-20
title: Das CO<sub>2</sub>-Ampel-Set
categories: hardware
description: Das CO<sub>2</sub>-Ampel-Set
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.kaufen/product/co2-ampel-bausatz
  - name: senseBox CO2 Ampel Programmcode V1
    link: /docs/sensebox_co2_ampel_v1.bin
image1: /images/2020-10-22-sets-co2-ampel/image1.jpg
image2: /images/2020-10-22-sets-co2-ampel/image2.jpg
image3: /images/2020-10-22-sets-co2-ampel/image3.jpg
image4: /images/2020-10-22-sets-co2-ampel/image4.jpg
image5: /images/2020-10-22-sets-co2-ampel/image5.jpg
image6: /images/2020-10-22-sets-co2-ampel/image6.jpg
image7: /images/2020-10-22-sets-co2-ampel/image7.jpg
image8: /images/2020-10-22-sets-co2-ampel/image8.jpg
image9: /images/2020-10-22-sets-co2-ampel/image9.jpg
image10: /images/2020-10-22-sets-co2-ampel/image10.jpg
image11: /images/2020-10-22-sets-co2-ampel/image11.jpg
image12: /images/2020-10-22-sets-co2-ampel/image12.jpg
image13: /images/2020-10-22-sets-co2-ampel/image13.jpg
image14: /images/2020-10-22-sets-co2-ampel/image14.jpg
image15: /images/2020-10-22-sets-co2-ampel/image15.jpg
image16: /images/2020-10-22-sets-co2-ampel/image16.jpg
image17: /images/2020-10-22-sets-co2-ampel/image17.jpg
image18: /images/2020-10-22-sets-co2-ampel/image18.jpg
image19: /images/2020-10-22-sets-co2-ampel/image19.jpg
image20: /images/2020-10-22-sets-co2-ampel/image20.jpg
image21: /images/2020-10-22-sets-co2-ampel/image21.png
image22: /images/2020-10-22-sets-co2-ampel/image22.png
image23: /images/2020-10-22-sets-co2-ampel/image23.jpg
image24: /images/2020-10-22-sets-co2-ampel/image24.jpg
image25: /images/2020-10-22-sets-co2-ampel/image25.jpg
image26: /images/2020-10-22-sets-co2-ampel/image26.jpg

---


{% include image.html image=page.image1 %}

# Benötigte Bauteile
{% include image.html image=page.image2 %}

-   senseBox Mikrocontroller (MCU) Lite
-   CO<sub>2</sub>-Sensor
-   RGB-LED
-   Display
-   3x JST-Verbindungskabel
-   Gehäuseteile
    -   6x Platten aus Plexiglas
    -   1x Stück Milchplexiglas
    -   11x Abstandshalter kurz
    -   4x Abstandshalter mittel
    -   4x Abstandshalter lang
    -   2x schwarze Plastikclips
    -   PCB Sensorhalterung
-   USB-Kabel
-   USB-Netzteil

# Aufbau

## 1.  Sensorhalterung vorbereiten

An die Sensorhalterung werden das Display, der CO<sub>2</sub>-Sensor und die RGB-LED angebracht. Später wird sie mit der Hauptplatine verbunden und
getestet.

Bringt als erstes auf der Oberseite die vier mittleren Abstandshalter
an:
{% include image.html image=page.image3 %}

Als Nächstes braucht ihr 6 kurze Abstandshalter und befestigt sie wie
folgt auf der gleichen Seite der PCB-Halterung:
{% include image.html image=page.image4 %}

Nun 5 kurze Abstandshalter auf der Unterseite anbringen:

{% include image.html image=page.image5 %}
Auf die Unterseite werden jetzt der CO<sub>2</sub> Sensor und die RGB-LED eingehängt:

{% include image.html image=page.image6 %}
{% include image.html image=page.image7 %}
Auf die Oberseite als Letztes das Milchplexiglas über der RGB-LED anbringen und das Display an das andere Ende. Achtet beim Display auf die korrekte Orientierung:

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

Steckt jetzt ein Verbindungskabel für die RGB-LED in einen der digitalen
Anschlüsse und zwei Verbindungskabel für Display und CO<sub>2</sub>-Sensor in einen
der drei I2C Steckplätze:

{% include image.html image=page.image6 %}

Jetzt könnt ihr die Kabel an den CO<sub>2</sub>-Sensor, das Display und die RGB-LED
anschließen. Hierbei darauf achten, dass die RGB-LED mit dem digitalen
Anschluss verbunden ist, bzw. das Display und der CO<sub>2</sub>-Sensor mit je
einem der I2C Anschlüsse:

{% include image.html image=page.image17 %}
{% include image.html image=page.image18 %}
Jetzt könnt ihr die Sensorhalterung mit der MCU über die langen
Abstandshalter verbinden. Achtet hierbei darauf, dass die Halterung
nicht falsch herum angebracht wird und sich genau parallel über die MCU
befindet:

{% include image.html image=page.image19 %}

## 3.  Software aufspielen und testen

Um die Ampel testen zu können, müsst ihr [hier](/docs/sensebox_co2_ampel_v1.bin) Programmdatei runterladen und auf die senseBox
übertragen. Schließt dazu die Messstation mit dem USB-Kabel an einen PC
an. Neben dem USB-Anschluss auf der MCU befindet sich ein roter Knopf.
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

Für den Fall, dass das Display schwarz bleibt, drückt einmal auf den oben
genannten Resetknopf, um das Programm auf der Station neu zu starten.

## 4.  senseBox ins Gehäuse einbauen

Als Nächstes werden die Seitenwände eingesetzt. Entfernt hierbei NICHT
die Folie von den Seitenteilen, da sie dann beim
Zusammenstecken fester sitzen bleiben:
{% include image.html image=page.image25 %}

Als Letztes vom Gehäusedeckel auf beiden Seiten die Schutzfolie
entfernen und ihn so anbringen, dass die Abstandshalter und die
Seitenteile einrasten:

{% include image.html image=page.image26 %}

Nun ist die CO<sub>2</sub>-Ampel einsatzbereit! Ihr könnt sie jetzt aufhängen und
über das USB-Kabel und das Netzteil an eine Steckdose anschließen.

