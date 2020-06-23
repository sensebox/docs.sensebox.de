---
date: 2020-03-11
title: MQTT integration
categories: opensensemap
description: MQTT integration for the openSenseMap
type: Document
---

This manual describes the possibility to send measured values via MQTT to the openSenseMap. The openSenseMap is able to connect to a public MQTT broker as an MQTT client. The openSenseMap does not offer an own MQTT broker. The openSenseMap MQTT client connects to a public MQTT Broker with a 13-digit Id with prefix 'osm_' followed by 8 random numbers and letters from A to F, unless otherwise specified in the connection settings.

Separate MQTT settings must be made for each registered senseBox. For a connection to a broker the following parameters can be specified. All specified settings are stored in the database of the openSenseMap. It is therefore advisable to set up your own access data.

## URL
The address to the MQTT Broker should start with 'mqtt://' or 'brows://'. If the MQTT Broker requires authentication by username and password, these can be encoded in the URL. The URL should then look like this: `mqtt://username:password@hostname.of.mqtt.broker`

## Topic
The MQTT Topic under which the openSenseMap messages should be received can be for example 'home/temperatures/outside'.

## Message format
Here you should choose between 'json' and 'csv'. The formats correspond to JSON array and csv documented in [docs.opensensemap.org](https://docs.opensensemap.org/#api-Measurements-postNewMeasurements).

## Decoding options
Expecting a JSON object. For json message format only: Allows a JSONPath expression to be specified under the jsonPath key, which specifies the position of the JSON-encoded data. Example: `{"jsonPath":"$.payload_fields"}`

## Connection options
Expecting a JSON object. Allows to pass connection options to the MQTT client. The keys `keepAlive`, `reschedulePings`, `clientId`, `username` and `password` from [https://github.com/mqttjs/MQTT.js#client](https://github.com/mqttjs/MQTT.js#client) are allowed.
