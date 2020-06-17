---
date: 2020-03-11
title: senseBoxMCU Library
categories: arduino
description: Usage of the senseBoxMCU Library
type: Document
resources:
  - name: "Shop"
    link: https://sensebox.kaufen/product/sensebox-mini
  - name: senseBoxMCU Library
    link: https://github.com/sensebox/SenseBoxMCU-Lib
---
# senseBox MCU Library
The senseBox MCU Library gives you access to the following functions/sensors:

- Temperature and humidity sensor [Sensor HDC1080](https://sensebox.shop/product/temperatur-luftfeuchte)
- Air pressure and temperature sensor [BMP280](https://sensebox.shop/product/luftdruck-temperatur)
- Brightness and UV Sensor [TSL45315 and VEML6070](https://sensebox.shop/product/licht-sensor)
- Ultrasonic distance sensor [HC SR04].
- Fine dust sensor [SDS011](https://sensebox.shop/product/feinstaub-sds011)
- senseBox GPS [CAM-M8Q](https://sensebox.shop/product/gps) --> required [TinyGPSPlus](https://github.com/mikalhart/TinyGPSPlus)
- Wifi connection via the WifiBee [WINC1500](https://sensebox.shop/product/wifi-bee) 
- Send data to the [openSenseMap](https://opensensemap.org)

## Use
The senseBoxMCU Library is part of the Board-Support-Package and is installed automatically. 

The senseBoxMCU library can be included individually with the following command:

```arduino
include <senseBoxMCU.h>
```

## Classes and functions
The library contains the following classes and functions. Create a new instance of a class to access its functions, e.g. the class 

```Arduino
#include "senseBoxMCU.h"

HDC1080 hdc;
```
 
Access to the following functions:

```Arduino
hdc.getTemperature();
hdc.getHumidity();
```

### Bee
```Arduino 
public:
	Bee();
		uint8_t connectToWifi(char* ssid, char* password);
		void startAP(char* ssid);
		char* getSsid();
		char* getPassword();
		char* getIpAddress();
```		

### OpenSenseMap
```Arduino 
Class name: OpenSenseMap

functions public:
			OpenSenseMap(const char* boxId, Bee* bee, const char* host);
			void uploadMeasurement(float value, char* sensorID);
			void uploadMobileMeasurement(float value, char* sensorID, float lat, float lng);
			void setUploadInterval(unsigned int);
```

### SDS011
```Arduino 
Class name: SDS011

functions public:
			SDS011(Stream& serial);
			float getPm10(void);
			float getPm25(void);
```

### HDC1080
```Arduino 
Class name: HDC1080

functions public:
			uint8_t begin(void);
			double getTemperature(void);
			double getHumidity(void); 
```

### VEML6070
```Arduino 
Class name: TSL45315

functions public:
			uint8_t begin(void);
			double getUvIntensity(void);
```

### TSL45315
```Arduino 
Class name: TSL45315

functions public:
			uint8_t begin(void);
			unsigned long getIlluminance(void); 
```

### Ultrasonic
```Arduino 
Class name: Ultrasonic

functions public:
			Ultrasonic(int rx, int tx);
        	long getDistance(void);
```

### BMP280
```Arduino 
Class name: BMP280

functions public:
			bool begin();
			float getTemperature(void);
			float getPressure(void);
			float getAltitude(float seaLevelhPa = 1013.25);
```

### GPS
```Arduino 
Class name: GPS

functions public:
			void begin();
			float getLatitude();
			float getLongitude();
			float getAltitude();
			float getSpeed();
			float getHdop();
			float getDate();
			float getTime();
```

### Mic

```Arduino

Class name: Microphones

functions public: 
		Microphones (int pin);
		float getValue();
```

### BMX

```Arduino

Classname BMX055

functions public:
		uint8_t beginAcc(char range);
		uint8_t beginGyro(void);
		uint8_t beginMagn(void);
		void getAcceleration(float *x, float *y, float *z, float *accTotal);
		void getMagnet(int *x, int *y, int *z);
		void getRotation(int *x, int *y, int *z);
```

### Button

```Arduino

Classname Button

functions public: 
		Button(int pin);
		void begin();
		bool getSwitch();
		bool isPressed();
		bool wasPressed();
```


