---
date: 2020-03-11
title: senseBox:home with LoRa
categories: sensebox-home
description: Send senseBox:home data via LoRa
type: Document
set: sensebox-home-general
set_order: 3
image00: /images/2020-03-11-home-erweiterung-lora/home-lora-00.png
image01: /images/2020-03-11-home-erweiterung-lora/home-lora-01.png
image02: /images/2020-03-11-home-erweiterung-lora/home-lora-02.png
image03: /images/2020-03-11-home-erweiterung-lora/home-lora-03.png
image04: /images/2020-03-11-home-erweiterung-lora/home-lora-04.png
image05: /images/2020-03-11-home-erweiterung-lora/home-lora-05.png
image06: /images/2020-03-11-home-erweiterung-lora/home-lora-06.png
image07: /images/2020-03-11-home-erweiterung-lora/home-lora-07.png
image08: /images/2020-03-11-home-erweiterung-lora/home-lora-08.png
image09: /images/2020-03-11-home-erweiterung-lora/home-lora-09.png
image10: /images/2020-03-11-home-erweiterung-lora/home-lora-10-en.png
image11: /images/2020-03-11-home-erweiterung-lora/home-lora-11.png
image12: /images/2020-03-11-home-erweiterung-lora/home-lora-12-en.png
image13: /images/2020-03-11-home-erweiterung-lora/home-lora-13-en.png
image14: /images/2020-03-11-home-erweiterung-lora/home-lora-14.png
image15: /images/2020-03-11-home-erweiterung-lora/home-lora-15.png
image16: /images/2020-03-11-home-erweiterung-lora/home-lora-16.png
---

## LoRa and TheThingsNetwork.org

If you want so use LoRa with your senseBox:home the data is sent via the [TheThingsNetwork](https://www.thethingsnetwork.org/) (TTN), therefore in the first step a **Device** must be created and a forwarding (**Integration**) of the data to the openSenseMap must be set up. In principle, all sensors that can be selected directly via the openSenseMap can be used. Decoding takes place directly on the openSenseMap and does **no longer ** have to be set via the TTN Console. 

## Registration on TheThingsNetwork.org

Many gateways set up by different groups, associations or companies use TheThingsNetwork to receive and send data. To receive and process data within the network, an account must first be created and the **devices** registered.

In very many cities there is already a good LoRa coverage. You can find an overview of the coverage on [ttnmapper.org](https://ttnmapper.org/). 
> Note that the coverage may not correspond to reality and the data may be out of date.

### Creating the application and a device

Create a new account at [https://www.thethingsnetwork.org/](https://www.thethingsnetwork.org/). Then click on Console and select **Applications**.

{% include image.html image=page.image00 %}

You get an overview of all already registered **Applications** and can add a new one via **add Application** in the top right corner. 

{% include image.html image=page.image01 %}

Choose a name for your application and add a short description. All other parameters can remain unchanged.
{% include image.html image=page.image03 %}

After a click on **Add Application** you get to the overview page. 
{% include image.html image=page.image04 %}

Several Devices can now be registered within an application. Click on **Devices** and select **register Device**. 
{% include image.html image=page.image05 %}

Give your **device** a one-time ID. The Device EUI, the APP Key and also the APP EUI are needed later and are generated automatically. 
{% include image.html image=page.image06 %}

### openSenseMap integration

The data is sent via TheThingsNetwork as simple bytes and from there it is forwarded to the openSenseMap. For this forwarding to take place click on **Integrations** and then create a new integration. 

Predefined **Integrations** are already created for some services. For the forwarding to the openSenseMap we use the simple **HTTP integration**. 

{% include image.html image=page.image07 %}

Give the integration a name and enter it under Process ID. Select the __default key__ as **Access Key**. The URL for the integration is 'https://ttn.opensensemap.org/v1.1'. All other parameters can remain unchanged. 

{% include image.html image=page.image09 %}

The registration to TheThingsNetwork is now complete. 


## Registration on the openSenseMap

The registration on the openSenseMap is done as described here. Select LoRa under connection type and add the sensors you connected to your senseBox in the first step. 
{% include image.html image=page.image10 %}

In order for the connection between TheThingsNetwork and the openSenseMap to work correctly, the next step is to select **senseBox:home** as decoding profile. Add your TTN Application ID and your TTN Device ID. Click on continue to complete the registration.

## Compile and transfer

After the registration you can compile your program code for the senseBox on the openSenseMap. Therefore you do not need to install any software on your computer. 

{% include image.html image=page.image12 %}
{% include image.html image=page.image13 %}

Copy the Device EUI, the Application EUI and the Application Key from the Device Overview and paste them into the corresponding fields and then press Compile.

### Transferring to the senseBox

Bring the senseBox into "learn mode" by double clicking the red reset button. The senseBox now appears as a removable disk and you can copy the previously downloaded program to the senseBox. The senseBox then restarts automatically and the data is transferred. 

>Beware: Under MacOS, the copying of the .BIN by Drag & Drop unfortunately does not work. The easiest way to do this is with our senseBox-Sketch Uploader. Just unzip the zip file and start the program. You can download the program [here](https://sensebox.de/docs/senseBox_Sketch_Uploader_DE.zip) directly. Alternatively, you can copy the file via [MuCommander](https://www.mucommander.com/) or via the terminal using 'd' (however, we recommend only experienced users\*).

## Problems

If your data does not appear on the openSenseMap, the first thing you should do is to check if your data has arrived at TheThingsNetwork. To do this, click on Data in your **Device Overview** and see if any data arrives there. Firstly, you should see an activation message marked with a flash. The incoming data is marked with Payload.

{% include image.html image=page.image14 %}

If data appears in the console but is not forwarded to the openSenseMap check if all parameters for the integration of TTN on the openSenseMap have been copied correctly. You can find the paremter in the dasboard of the openSenseMap.

Click on Edit on your senseBox and then select TheThingsNetwork from the side menu. 
