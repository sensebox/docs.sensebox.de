---
date: 2020-03-11
title: "Step 2: Registration on the openSenseMap"
title_order: 2
categories: sensebox-home
description: Step 2 for building the senseBox:home
type: Document
set: aufbau-sensebox-home
set_order: 2
image1: /images/sensebox-home/osem-1-en.png
image2: /images/sensebox-home/osem-2-en.png
image3: /images/sensebox-home/osem-3-en.png
image4: /images/sensebox-home/osem-4-en.png
image5: /images/sensebox-home/osem-5-en.png
---

After your senseBox:home has been assembled, it needs be registered on the [openSenseMap](https://opensensemap.org). 

The openSenseMap is a platform to store, compare and visualize sensor data. It is best to have a look at it. Go to [www.opensensemap.org](https://www.opensensemap.org) and discover a huge pool of sensor data from all over the world. Not only senseBoxes send data to the openSenseMap, but also other microcontrollers with sensors. How the individual functions of the openSenseMap and their interfaces work, you can find [here](https://docs.sensebox.de/opensensemap/).

{% include image.html image=page.image1 %}


## 1.User account registration
Go to [www.opensensemap.org](https://www.opensensemap.org) and create an account. To do this, click on "Login" in the top right corner and then go to "Sign up". You need a valid e-mail address to register. After successful registration you will receive an e-mail with a confirmation link. Please click on the link to complete the registration. 


{% include image.html image=page.image2 %}

## 2. Create a new senseBox
After the successful registration you can start creating your senseBox. To do so, click on "New senseBox" in your menu and confirm the terms of use. Then follow the instructions of the registration and enter the following data:

* A freely selectable name for the senseBox
* The environment (exposure) in which you want to set up your senseBox
* The location where you want to set up your senseBox (you can also have your location determined automatically)


{% include image.html image=page.image3 %}

Since the openSenseMap is open for all kinds of senseBoxes, you will be asked for the hardware used. Select *senseBox:home V2* and the data transfer module you are using. If you want to send your data via LoRa to the openSenseMap, select LoRa at "connection type". Then you can specify your Lora settings in the "Advanced" tab. Here you have to enter the Application-ID and Device-ID which you have entered at <a href="www.thethingsnetwork.org">TheThingsNetwork</a>. More information can be found [here](/sensebox-home-extensions/home-extensions-lora/)

{% include image.html image=page.image4 %}

For some sensors you still have to select to which port you have connected them. 
{% include image.html image=page.image5 %}


## 3. Summary of the registration 
Once you have completed the registration process, you will have to agree to the publication of your data again. Afterwards you will receive an overview of your registration. There you will see your senseBox ID, your sensor IDs and the Arduino code.  

The senseBox ID is a unique identifier of your senseBox. You can use it to find your senseBox e.g. via the URL (opensensemap.org/explore/ENTER HERE YOUR-SENSEBOX-ID) or in records. Furthermore it is used for various applications and functions around the senseBox and the openSenseMap.


<hr>
<a href="/sensebox-home/home-schritt-1/" class="button">Back to step 1</a>
<a href="/sensebox-home/home-schritt-3/" style="float: right;" class="button">Continue with step 3</a>
