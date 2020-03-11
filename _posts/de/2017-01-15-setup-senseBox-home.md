---
date: 2017-01-15
title: Setup senseBox:home
video_id: _iH8f5alzWA
description: Have non-technical people update Jekyll sites
categories:
  - senseBox:home
resources:
  - name: Source code
    link: https://github.com/CloudCannon/creative-jekyll-theme/
  - name: CloudCannon
    link: https://cloudcannon.com
type: Document
set: sensebox-home-instructions
set_order: 1
lang: de
---
In wenigen Schritten lernst du deine senseBox:home... 

## Vorbereitung



## Setup

### Schritt 2: Board-Support-Package installieren {#head}

<div class="description">Damit die Arduino IDE deine <a href="../komponenten/sensebox-mcu.md">senseBox MCU</a> unterstützt und du Programme auf diese übertragen kannst, musst du vor Beginn noch zwei Board-Support-Packages installieren. Diese beinhalten die nötigen Treiber und die notwendige Software, um mit deinem Prozessor zu kommunizieren. Das Board-Support-Package der senseBox enthält außerdem bereits unsere senseBox-Libraries. Damit stehen euch alle grundlegenden Methoden zur Programmierung der beiliegenden Sensoren zur Verfügung.</div>
<div class="line">
    <br>
    <br>
</div>

### Libraries

Für die Programmierung der senseBox sollten zu Beginn unbedingt die senseBox-Libraries eingebunden werden. Diese Libraries haben wir für euch in das Board-Support-Package der senseBox integriert, um euch die Installation möglichst einfach zu gestalten. 


Eine Library ist wie der Name schon sagt eine Sammlung von etwas - eine Sammlung von Methoden um genauer zu sein. Methoden sind in der Programmierung kleinere Abschnitte von Code, die auf ein Objekt angewendet werden können. 
Bei der senseBox zum Beispiel kann eine Methode aufgerufen werden, um die LEDs auf dem MCU ein- und auszuschalten. Es gibt eine Menge solcher Standardmethoden, die von einer Vielzahl an Programmmen benutzt werden. Um diese Methoden nicht alle einzeln in den Programmcode übertragen zu müssen, können sie in Libraries abgelegt werden. 
Eine Library ist also eine Datei, in der viele Methoden gespeichert werden. Man kann Libraries in seinen Code einbinden. Dafür reicht es, wenn sie im Arduino-Ordner für Libraries gespeichert sind und man sie dann mit einer einzigen Zeile zu Beginn des Programmcodes einbindet. Das sieht in Arduino für die Library mit dem Namen "senseBoxIO" wie folgt aus: 

```arduino
#include <senseBoxMCU.h>;
```

Ist die Library eingebunden, können alle in ihr enthaltenen Methoden im Code benutzt werden. 


### Board-Support-Package einbinden 
Wähle dein Betriebssystem, um die passende Anleitung zu sehen:

#### Anleitung für Windows
Füge die folgende URL in deiner Arduino IDE unter *Datei -> Voreinstellungen* in das Feld für *Zusätzliche Bordverwalter-URLs* ein:
```
https://github.com/sensebox/senseBoxMCU-core/raw/master/package_sensebox_index.json
```

![Öffne die Voreinstellungen und füge die URL ein](https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/Ardu1.png)

Öffne dann den *Boardverwalter* unter *Werkzeuge -> Board:"..." -> Boardverwalter* und installiere dort die zwei Board-Support-Packages mit den Namen **Arduino SAMD Boards by Arduino** und **senseBox SAMD Boards by senseBox**.

![Öffne den Bordverwalter und installiere die beiden Packages](https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/Ardu2.png)

<div class="box_info">
    <i class="fa fa-info fa-fw" aria-hidden="true" style="color: #42acf3;"></i>
  Gib "SAMD" oben in die Suchleiste ein um die Packages schneller zu finden
</div>

Da wir das **senseBox SAMD Boards**-Package für euch regelmäßig aktualisieren, solltet ihr immer mal wieder in den Boardverwalter gehen und nachschauen, ob das **senseBox SAMD Boards**-Package noch aktuell ist. Öffnet dafür, wie oben beschrieben, den Boardverwalter und sucht nach **senseBox SAMD Boards**. Wenn ihr auf den Eintrag in der Liste klickt, erscheint dort, im Falle einer neuen Version, ein Update-Button. Klickt diesen, um die neuste Version zu installieren. 

![Klicke auf 'Update', um das Board-Support-Package zu aktualisieren](https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/update-b-s-p.png)

<div class="box_info">
    <i class="fa fa-info fa-fw" aria-hidden="true" style="color: #42acf3;"></i>
  Wichtig ist, zuerst auf den Eintrag zu klicken. Ansonsten wird der Update-Button nicht angezeigt, auch wenn es bereits eine neue Version gibt.
</div> 

#### Anleitung für Mac
Füge die folgende URL in deiner Arduino IDE unter *`Arduino -> Einstellungen...`* in das Feld für *Zusätzliche Bordverwalter-URLs* ein:
```
https://github.com/sensebox/senseBoxMCU-core/raw/master/package_sensebox_index.json
```

![Öffne die Voreinstellungen und füge die URL ein](https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/ardu_mac.png)

Öffne dann den *Boardverwalter* unter *Werkzeuge -> Board:"..." -> Boardverwalter* und installiere dort die zwei Board-Support-Packages mit den Namen **Arduino SAMD Boards by Arduino** und **senseBox SAMD Boards by senseBox**.

![Öffne den Bordverwalter ](https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/ardu3_mac.png)

![Installiere die beiden markierten Packages](https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/ardu2_mac.png)


<div class="box_info">
    <i class="fa fa-info fa-fw" aria-hidden="true" style="color: #42acf3;"></i>
  Gib "SAMD" oben in die Suchleiste ein um die Packages schneller zu finden
</div>

Da wir das **senseBox SAMD Boards**-Package für euch regelmäßig aktualisieren, solltet ihr immer mal wieder in den Boardverwalter gehen und nachschauen, ob das **senseBox SAMD Boards**-Package noch aktuell ist. Öffnet dafür, wie oben beschrieben, den Boardverwalter und sucht nach **senseBox SAMD Boards**. Wenn ihr auf den Eintrag in der Liste klickt, erscheint dort, im Falle einer neuen Version, ein Update-Button. Klickt diesen, um die neuste Version zu installieren. 

![Klicke auf 'Update', um das Board-Support-Package zu aktualisieren](https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/ardu_update_mac.png)

<div class="box_info">
    <i class="fa fa-info fa-fw" aria-hidden="true" style="color: #42acf3;"></i>
  Wichtig ist, zuerst auf den Eintrag zu klicken. Ansonsten wird der Update-Button nicht angezeigt, auch wenn es bereits eine neue Version gibt.
</div>

#### Anleitung für Linux
Füge die folgende URL in deiner Arduino IDE unter *Datei -> Voreinstellungen* in das Feld für *Zusätzliche Bordverwalter-URLs* ein:
```
https://github.com/sensebox/senseBoxMCU-core/raw/master/package_sensebox_index.json
```

![Öffne die Voreinstellungen und füge die URL ein](https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/Ardu1.png)

Öffne dann den *Boardverwalter* unter *Werkzeuge -> Board:"..." -> Boardverwalter* und installiere dort die zwei Board-Support-Packages mit den Namen **Arduino SAMD Boards by Arduino** und **senseBox SAMD Boards by senseBox**.

![Öffne den Bordverwalter und installiere die beiden Packages](https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/Ardu2.png)

<div class="box_info">
    <i class="fa fa-info fa-fw" aria-hidden="true" style="color: #42acf3;"></i>
  Gib "SAMD" oben in die Suchleiste ein um die Packages schneller zu finden
</div>

Da wir das **senseBox SAMD Boards**-Package für euch regelmäßig aktualisieren, solltet ihr immer mal wieder in den Boardverwalter gehen und nachschauen, ob das **senseBox SAMD Boards**-Package noch aktuell ist. Öffnet dafür, wie oben beschrieben, den Boardverwalter und sucht nach **senseBox SAMD Boards**. Wenn ihr auf den Eintrag in der Liste klickt, erscheint dort, im Falle einer neuen Version, ein Update-Button. Klickt diesen, um die neuste Version zu installieren. 

![Klicke auf 'Update', um das Board-Support-Package zu aktualisieren](https://github.com/sensebox/resources/raw/master/gitbook_pictures/ardu/update-b-s-p.png)

<div class="box_info">
    <i class="fa fa-info fa-fw" aria-hidden="true" style="color: #42acf3;"></i>
  Wichtig ist, zuerst auf den Eintrag zu klicken. Ansonsten wird der Update-Button nicht angezeigt, auch wenn es bereits eine neue Version gibt.
</div>



## Editables

Next, we need to do is to define areas in our HTML which non-developers can update. These are called [Editable Regions](https://docs.cloudcannon.com/editing/editable-regions/) and are set by adding a class of `editable` to HTML elements.

Open `index.html` in CloudCannon and add a class of `editable` to the `h1` and `p` inside `<div class="header-content-inner">` so it becomes the following:

~~~ html
<div class="header-content-inner">
  <h1 class="editable">Your Favorite Source of Free Bootstrap Themes</h1>
  <hr>
  <p class="editable">Start Bootstrap can help you build better websites using the Bootstrap CSS framework! Just download your template and start going, no strings attached!</p>
  <a href="/about.html" class="btn btn-primary btn-xl page-scroll">Find Out More</a>
</div>
~~~

## Client Access

Now the site is ready for our non-developer to update. We'll set up [Client Sharing](https://docs.cloudcannon.com/sharing/client-sharing/) which allows our client to update their site without having to create an account. Go to the Site Settings / Client Sharing section and set a password for your client.

Our non-developer can view their live site at your-site.cloudvent.net (or you can set up a custom domain). To update their site they just add `/update` to the URL and enter the password we set earlier.

## The Client Workflow

Once the client logs in they see their site with colored boxes highlighting the editable regions. The client can update content directly inline by clicking on text:

By clicking _Collections_ in the sidebar the client can manage their blog posts:

Editing posts happens in the [Content Editor](https://docs.cloudcannon.com/editing/content-editor/) which is a rich text editor for Markdown. The client can also manage all the front matter data on the page using an easy-to-use editor:

Or we can use the [Visual Editor](https://docs.cloudcannon.com/editing/visual-editor/) to update posts:

The client can also update collection items using the same editor. In this example there's no body content and only front matter so we've made the front matter editor full screen:

If we have GitHub, Bitbucket or Dropbox connected to the site, all changes the client makes are pushed back to the storage provider.

Now the client can update all the content and hasn't had to learn HTML, Liquid or Markdown. This gives a small taste of what you can achieve on CloudCannon. [Sign up free](https://app.cloudcannon.com/users/sign_up) and make your Jekyll site client editable.