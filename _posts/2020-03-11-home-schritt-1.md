---
date: 2020-03-11
title: 'Step 1: Hardware setup'
title_order: 1
categories: sensebox-home
description: Step 1 for setting up the senseBox:home.
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


## Welcome to the tutorial for the assembly of senseBox:home

Since the senseBox is a modular kit, individual steps to sensors may differ or even be skipped in your case. First we show you how to insert the microcontroller into the case.
{% include image.html image=page.image1 %}
To do this, take the housing and align it with the bore pointing downwards. The green senseBox microcontroller is now placed on the opposite side, so that the red reset button and the USB port are facing the front. 

{% include image.html image=page.image2 %}

Now you take the two smaller screws included and fix the board to the case via the middle drill holes. If the board has some clearance it is no problem. 

## Setting up the WiFi-Bee
Next we will show how to set up the Wifi-Bee. 

We have printed a label on all Bees to indicate the direction. If you have another data transfer module, e.g. LAN, or LoRaWAN, this is exactly the same. 
{% include image.html image=page.image3 %}

The Wifi-Bee is placed on XBee port 1 and carefully pressed into the baseboard so that all pins of the Bees are inserted.

{% include image.html image=page.image4 %}


## Setup of the radiation protection housing

Now we show the construction of the radiation protection housing in which the temperature and humidity sensor is mounted.
In the radiation protection there are some mounting parts to mount it later outside. These we do not need for the time being. 

{% include image.html image=page.image5 %}

First, a long senseBox cable is pulled through the opening in the base of the radiation shield and the temperature and humidity sensor is plugged in.

{% include image.html image=page.image6 %}

The sensor can now also be attached to the stand with some adhesive tape or a cable tie. The radiation protection housing later ensures good air circulation and at the same time protects the sensor from the weather.
Now the radiation protection housing can be plugged together and later the sensor is connected to the senseBox microcontroller.

## Setup of the fine dust sensor

Next we show the setup of the fine dust sensor. 
{% include image.html image=page.image7 %}


{% include image.html image=page.image8 %}
For this purpose, the housing for the sensor must be provided with openings for cables and the air supply. 
The openings should be opposite each other on the sides with two predetermined breaking points each. 
For safety reasons we recommend drilling the openings. Theoretically, the openings can also be opened at the predetermined breaking points with a blunt object.  


Next, we take the fine dust sensor and place it in the housing so that the cable connection and the air intake socket are at the openings that have just been drilled.

{% include image.html image=page.image9 %} 

The cable for the fine dust sensor has a different colour and is attached to the sensor with the larger connector. 


Then the cable glands for the cable connection are fitted.
Simply unscrew the cable gland and then sort the individual parts in the correct order. Then quickly screw them together and that's it.

{% include image.html image=page.image10 %} 
On the other side of the sensor, the hose is now attached to the air intake socket.
Here we also use a cable gland to seal the hose. Then we have to sort everything correctly. At the end, some pressure on the tube is necessary to put it on the socket. Finally put on the lid and the fine dust sensor is ready.

{% include image.html image=page.image11 %} 
## Connecting the external sensors to the MCU

{% include image.html image=page.image12 %} 
The external sensors, i.e. the sensor for temp. and humidity and the fine dust sensor are now connected to the MCU.
For this, we first take the cable out of the radiation protection and thread it through the last cable gland into the housing.
{% include image.html image=page.image13 %} 
There the cable is plugged into one of the slots marked I2C/Wire. 
{% include image.html image=page.image14 %} 


Then the cable is taken out of the fine dust sensor and threaded through the gland. 
This cable is inserted into one of the slots labeled UART/Serial. 

{% include image.html image=page.image15 %} 

## Connecting the USB cable

{% include image.html image=page.image16 %} 

Finally, we connect the micro-USB cable, which is used to program the microcontroller and to supply the senseBox with power later during operation. 
Please note that the micro-USB port is sensitive and is also subject to the leverage of the cable. For this reason, the USB cable should not be torn later.
{% include image.html image=page.image17 %} 

## Connecting the internal sensors to the MCU

{% include image.html image=page.image18 %} 
After the outer sensors are connected, the remaining sensors are mounted inside the housing.
A mounting level is constructed for this purpose. First, four spacers are inserted into the external holes of the microcontroller. 
The spacers have a grid mechanism. Therefore, if they have to be loosened, they should not be torn out by force, but slightly pressed in at the head.  
Afterwards we connect two senseBox cables to the I2C/Wire slots to attach the air pressure sensor and the light sensor.
{% include image.html image=page.image19 %} 

The cables are threaded through the middle recesses of the mounting plate. 
{% include image.html image=page.image20 %} 
Then the mounting plate is pressed onto the spacers and the cables are connected to the sensors. 
The sensors are each equipped with two spacers and fastened to the mounting plate. 
If you have chosen a light sensor, it should be placed as centrally as possible in the housing to obtain good measured values.
The air pressure sensor can be placed in the outer slot.
{% include image.html image=page.image21 %} 

Finally, the cover is fitted with the screws and a silica gel bag is placed inside the housing for further protection against moisture.
{% include image.html image=page.image22 %} 
{% include image.html image=page.image23 %} 
Now the quick release screws are screwed in and the senseBox is closed. 


<hr>
<a href="/sensebox-home/home-schritt-2/" class="button" style="float: right;">continue with step 2</a>