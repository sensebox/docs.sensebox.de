---
date: 2020-10-16
title: Security 
categories: opensensemap
description: Secure data upload to openSenseMap
type: Document
title_order: 10
resources:
image1: /images/2020-10-16-opensensemap-security/security_osem_en.jpg
---

It is possible to protect the data upload to your senseBox with a generated auth token. This option can be enabled on the openSenseMap in your personal dashboard. You also have the ability to generate a new token, but be careful, this can not be undone.

{% include image.html image=page.image1 %}

## How to use the Token?

As soon as you enable the authentication, all the POST-Requests for your senseBox have to include your authentication token. Otherwise the openSenseMap will reject the data submitted. The two endpoint which require this token are `https://api.opensensemap.org/boxes/:senseBoxId/:sensorId` and `https://api.opensensemap.org/boxes/:senseBoxId/data`.
An Example header would look like this:

```
'Authorization' : 'YOUR_BOX_ACCESS_TOKEN'
```

## MQTT und TTN

If you use the MQTT or TTN extension to upload your data to the openSenseMap you will not need this token, but it is advised to enable the authentication in order to prevent third parties from sending data to your senseBox.
