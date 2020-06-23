---
date: 2020-03-11
title: Registration of a new senseBox
categories: opensensemap
description: Registration of a new senseBox
type: Document
---

To register a new senseBox on the openSenseMap, a user account must first be created under *Login*.
Afterwards you can find the dashboard under the user logo in the upper right corner, where senseBoxes can be added and [managed](/opensensemap/opensemap-manage/).

Under *New senseBox* a new senseBox can now be registered. The following information is necessary:

- **Name of the senseBox**: e.g. the location
- **Site**: serves to filter boxes
- **Location**: can be selected via the map
- **Model**: determines the sensor configuration

There is a pre-selection for different models.
If a sensor configuration is not available, individual sensors can be added manually under *Manual Configuration*.

After the registration has been completed, an Arduino sketch is displayed which reads the specified sensors and regularly transfers their data to the openSenseMap.
To transfer this to the senseBox, the [Arduino IDE](https://www.arduino.cc/en/Main/Software) is required, an example installation guide for the *senseBox:home* can be found [here](https://home.books.sensebox.de/de/software_installation.html).

## Advanced Configuration
It is possible to use other interfaces for data transmission besides the [HTTP REST API](https://docs.opensensemap.org/).
Settings for this must be made under the corresponding tab in the *Advanced* section.
Detailed instructions can be found here:

- [MQTT](mqtt_client.md)
- [TheThingsNetwork](ttn_integration.md)
