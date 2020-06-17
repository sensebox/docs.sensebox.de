---
date: 2020-03-11
title: senseBoxIO Library
categories: arduino
description: Usage of the senseboxIO Library
type: Document
resources:
  - name: "senseBoxIO Library"
    link: https://github.com/sensebox/senseBoxMCU-core/tree/master/arduino/samd/libraries/senseBoxIO
---

> The senseBoxIO Library is part of the Board Support Package and is installed automatically. 

The senseBoxIO library can be included individually using the following command:

```arduino
include <senseBoxIO.h>
```

> Note: If you already use the senseBoxMCU Library, the senseBoxIO Library is already integrated and does not need to be included

## Switching ports on/off

Unused ports can be switched on/off via the senseBoxIO library:

#### Disable all ports
```arduino
 void powerNone(void)
```  
#### Activate all ports

```arduino
  void powerAll(void)
```  
#### Selective on/off switching of ports and connectors

```arduino

  void powerI2C(bool on) //power the I2C Ports
  
  void powerUART(bool on) //power the UART Ports

  void powerXB1(bool on) //power XBEE Port 1
 
  void powerXB2(bool on) //power XBEE Port 2
 
  void SPIselectNone(void) //
 
  void SPIselectXB1(void) //
 
  void SPIselectXB2(void) //

```

## Switch on/off the status LED

Allows to switch on/off the status LEDs


```arduino
  void statusNone(void) // deactivate all status LED's

  void statusRed(void) //activate the red status LED

  void statusGreen(void) //activate the green status LED
```
