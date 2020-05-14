---
date: 2020-03-11
title: Installation des Board-Support-Packages
title_order: 4
categories: erste-schritte-arduino
description: Installation des Board-Support-Packages für die senseBox MCU
type: Document
set: erste-schritte-arduino
set_order: 4
---

<div class="description">Damit die Arduino IDE deine senseBox MCU unterstützt und du Programme auf diese übertragen kannst, musst du vor Beginn noch zwei Board-Support-Packages installieren. Diese beinhalten die nötigen Treiber und die notwendige Software, um mit dem Prozessor der senseBox zu kommunizieren. Das Board-Support-Package der senseBox enthält außerdem bereits unsere senseBox-Libraries. Damit stehen euch alle grundlegenden Methoden zur Programmierung der beiliegenden Sensoren zur Verfügung.</div>



## Anleitung für Windows
Füge die folgende URL in deiner Arduino IDE unter *Datei -> Voreinstellungen* in das Feld für *Zusätzliche Bordverwalter-URLs* ein:
```
https://github.com/sensebox/senseBoxMCU-core/raw/master/package_sensebox_index.json
```
<br>
<style>
img.click-zoom {
 transition: transform 0.2s;
}
img.click-zoom:active {
 transform: scale(2.0, 2.0);
}
</style>

<img src="https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/Ardu1.png" class="click-zoom">


Öffne dann den *Boardverwalter* unter *Werkzeuge -> Board:"..." -> Boardverwalter* und installiere dort die zwei Board-Support-Packages mit den Namen **Arduino SAMD Boards by Arduino** und **senseBox SAMD Boards by senseBox**.

<style>
img.click-zoom {
 transition: transform 0.2s;
}
img.click-zoom:active {
 transform: scale(2.0, 2.0);
}
</style>

<img src="https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/Ardu2.png" class="click-zoom">


  Gib "SAMD" oben in die Suchleiste ein um die Packages schneller zu finden.


Da wir das **senseBox SAMD Boards**-Package für euch regelmäßig aktualisieren, solltet ihr immer mal wieder in den Boardverwalter gehen und nachschauen, ob das **senseBox SAMD Boards**-Package noch aktuell ist. Öffnet dafür, wie oben beschrieben, den Boardverwalter und sucht nach **senseBox SAMD Boards**. Wenn ihr auf den Eintrag in der Liste klickt, erscheint dort im Falle einer neuen Version ein Update-Button. Klickt diesen, um die neuste Version zu installieren. 


<style>
img.click-zoom {
 transition: transform 0.2s;
}
img.click-zoom:active {
 transform: scale(2.0, 2.0);
}
</style>
<img src="https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/update-b-s-p.png" class="click-zoom">

  Wichtig ist, zuerst auf den Eintrag zu klicken. Ansonsten wird der Update-Button nicht angezeigt, auch wenn es bereits eine neue Version gibt.



## Anleitung für Mac
Füge die folgende URL in deiner Arduino IDE unter *`Arduino -> Einstellungen...`* in das Feld für *Zusätzliche Bordverwalter-URLs* ein:
```
https://github.com/sensebox/senseBoxMCU-core/raw/master/package_sensebox_index.json
```
<br>
<style>
img.click-zoom {
 transition: transform 0.2s;
}
img.click-zoom:active {
 transform: scale(2.0, 2.0);
}
</style>
<img src="https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/ardu_mac.png" class="click-zoom">


Öffne dann den *Boardverwalter* unter *Werkzeuge -> Board:"..." -> Boardverwalter* und installiere dort die zwei Board-Support-Packages mit den Namen **Arduino SAMD Boards by Arduino** und **senseBox SAMD Boards by senseBox**.

<style>
img.click-zoom {
 transition: transform 0.2s;
}
img.click-zoom:active {
 transform: scale(2.0, 2.0);
}
</style>
<img src="https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/ardu3_mac.png" class="click-zoom">

<style>
img.click-zoom {
 transition: transform 0.2s;
}
img.click-zoom:active {
 transform: scale(2.0, 2.0);
}
</style>
<img src="https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/ardu2_mac.png" class="click-zoom">



  Gib "SAMD" oben in die Suchleiste ein um die Packages schneller zu finden.


Da wir das **senseBox SAMD Boards**-Package für euch regelmäßig aktualisieren, solltet ihr immer mal wieder in den Boardverwalter gehen und nachschauen, ob das **senseBox SAMD Boards**-Package noch aktuell ist. Öffnet dafür, wie oben beschrieben, den Boardverwalter und sucht nach **senseBox SAMD Boards**. Wenn ihr auf den Eintrag in der Liste klickt, erscheint dort im Falle einer neuen Version ein Update-Button. Klickt diesen, um die neuste Version zu installieren. 

<style>
img.click-zoom {
 transition: transform 0.2s;
}
img.click-zoom:active {
 transform: scale(2.0, 2.0);
}
</style>
<img src="https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/ardu_update_mac.png" class="click-zoom">


  Wichtig ist, zuerst auf den Eintrag zu klicken. Ansonsten wird der Update-Button nicht angezeigt, auch wenn es bereits eine neue Version gibt.



## Anleitung für Linux
Füge die folgende URL in deiner Arduino IDE unter *Datei -> Voreinstellungen* in das Feld für *Zusätzliche Bordverwalter-URLs* ein:
```
https://github.com/sensebox/senseBoxMCU-core/raw/master/package_sensebox_index.json
```
<br>
<style>
img.click-zoom {
 transition: transform 0.2s;
}
img.click-zoom:active {
 transform: scale(2.0, 2.0);
}
</style>
<img src="https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/Ardu1.png" class="click-zoom">

Öffne dann den *Boardverwalter* unter *Werkzeuge -> Board:"..." -> Boardverwalter* und installiere dort die zwei Board-Support-Packages mit den Namen **Arduino SAMD Boards by Arduino** und **senseBox SAMD Boards by senseBox**.

<style>
img.click-zoom {
 transition: transform 0.2s;
}
img.click-zoom:active {
 transform: scale(2.0, 2.0);
}
</style>
<img src="https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/Ardu2.png" class="click-zoom">



Gib "SAMD" oben in die Suchleiste ein um die Packages schneller zu finden.
<br>

Da wir das **senseBox SAMD Boards**-Package für euch regelmäßig aktualisieren, solltet ihr immer mal wieder in den Boardverwalter gehen und nachschauen, ob das **senseBox SAMD Boards**-Package noch aktuell ist. Öffnet dafür, wie oben beschrieben, den Boardverwalter und sucht nach **senseBox SAMD Boards**. Wenn ihr auf den Eintrag in der Liste klickt, erscheint dort im Falle einer neuen Version ein Update-Button. Klickt diesen, um die neuste Version zu installieren. 

<style>
img.click-zoom {
 transition: transform 0.2s;
}
img.click-zoom:active {
 transform: scale(2.0, 2.0);
}
</style>
<img src="https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/update-b-s-p.png" class="click-zoom">

Wichtig ist, zuerst auf den Eintrag zu klicken. Ansonsten wird der Update-Button nicht angezeigt, auch wenn es bereits eine neue Version gibt.



