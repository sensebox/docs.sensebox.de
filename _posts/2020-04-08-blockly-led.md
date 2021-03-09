---
date: 2020-04-07
title: LED
title_order: 4
categories: Blockly
description: Erste Schritte LED
type: Document

resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de
image1: /images/2020-04-08-blockly-led/blockly-led-1.svg
image2: /images/2020-04-08-blockly-led/blockly-led-2.svg
image3: /images/2020-04-08-blockly-led/blockly-led-3.svg

---

## LED
Mit dem `LED an digitalen Pin`-Block kannst du eine an einem der sechs digitalen Pins angeschlossene LED ansteuern. Im Dropdown-Menü __Pin__ wählst du den jeweiligen Pin aus und unter __Status__, ob die LED ein- oder ausgeschaltet werden soll.

{% include image.html image=page.image1 %}

> BUILTIN_1 und BUILTIN_2 sind die auf der senseBox MCU fest verbauten LEDs neben dem roten RESET-Knopf.

## RGB-LED
Mit dem `RGB-LED`Block kannst du eine an einem der sechs digitalen Pins angeschlossene RGB-LED ansteuern. Im Dropdown-Menü __Pin__ wählst du den jeweiligen Pin aus. An die Blockabschnitte __rot__, __grün__ und  __blau__ können Zahlen von 0 bis 255 angeknüpft werden, um die Intesität der verschiedenen Farbanteile festzulegen. Bei einem Wert von 0 ist kein Farbanteil vorhanden, bei einem Wert von 255 ist der maximale Farbanteil vorhanden.

{% include image.html image=page.image2 %}

> Der Farbcode für senseBox Grün lautet zum Beispiel:  
{% include image.html image=page.image3 %}
