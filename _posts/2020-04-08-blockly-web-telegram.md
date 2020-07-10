---
date: 2020-04-07
title: Web - Telegram
title_order: 5
categories: Blockly
description: Erste Schritte Telegram
type: Document

resources:
  - name: "Blockly.senseBox.de"
    link: https://blockly.sensebox.de

image5: /images/2020-04-08-blockly-web/blockly-Web-Telegram-1-en.svg
image6: /images/2020-04-08-blockly-web/blockly-Web-Telegram-2-en.svg
image7: /images/2020-04-08-blockly-web/blockly-Web-Telegram-3-en.svg
image8: /images/2020-04-08-blockly-web/blockly-Web-Telegram-4-en.svg

---

## Telegram
With [Telegram](https://www.telegram.org) you can build a chatbot, which helps you to read your senseBox from everywhere via text message. 

> Telegram is a free messenger, which offers the possibility to create chatbots in the easiest way. To use it you need a Telegram account. When you create your chatbord a token will be displayed which you can use in Blockly to authenticate yourself. More about creating a chatbot can be found in the project [Telegram chatbot for the senseBox with Blockly](https://sensebox.de/projects/de/2019-12-15-telegram-blockly).

With the 'Initialize Telegram Bot' block in Setup() the senseBox is prepared to send data to the chatbot on request. In the text field "Token" you have to enter the token that is displayed when creating your chatbot.

{% include image.html image=page.image5 %}

Afterwards, the block 'Telegram do' can be used to program in the endless loop() what exactly the chatbot should do.

{% include image.html image=page.image6 %}

The `On Message` and `Send Message` blocks can be placed in the free block section of the 'Make Legam' block to specify what the senseBox should do when it receives a particular message.

<table style="border-collapse:collapse;border-spacing:0;border:none" class="tg"><tr><th style="font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;text-align:left;vertical-align:middle">{% include image.html image=page.image7 %}</th><th style="font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;text-align:left;vertical-align:top">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</th><th style="font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;text-align:left;vertical-align:top">{% include image.html image=page.image8 %}</th></tr></table>

With the `On Message` block you can define an action that the senseBox should perform when a certain message arrives via telegram. For example switching a LED on or off.

With the `Send Message` block a message can be sent via telegram to the user of the bot.