---
date: 2020-04-07
title: Schleifen
title_order: 5
categories: Blockly
description: Verwendung von Schleifen in Blockly
type: Document
set: blockly-erste-schritte
set_order: 5
image1: /images/2020-04-08-blockly-schleifen/blockly-schleifen-1.svg
image2: /images/2020-04-08-blockly-schleifen/blockly-schleifen-2.svg
image3: /images/2020-04-08-blockly-schleifen/blockly-schleifen-3.svg
---

## Allgemeines
Schleifen gehören zu den wichtigsten Kontrollstrukturen beim Programmieren. Sie helfen dir immer dann, wenn du eine oder mehrere Anweisungen eine gewisse Anzahl von Wiederholungen oft ausführen lassen willst. In Blockly gibt es verschiedene Arten von Schleifen, deren Funktionsweisen allerdings immer sehr ähnlich sind. Du findest alle Schleifen in der gleichnamigen Kategorie in der Toolbox.

## Wiederhole X mal Schleife
Die einfachste Schleife ist die `Wiederhole X mal`-Schleife. In ihr werden alle Befehle innerhalb der Schleife X-mal wiederholt.

{% include image.html image=page.image1 %}

## Wiederhole solange Schleife
Die zweite  Schleife ist die `Wiederhole solange/bis`-Schleife. Die in der Schleife eingefügten Befehle werden nur dann ausgeführt, wenn eine im freien Blockabschnitt angeknüpfte Bedingung zutrifft/wahr ist. Im Dropdown-Menü des Blockst lässt sich auswählen ob die Befehle ausgeführt werden soll **bis** eine Bedingung zutrifft, oder **solang** eine Bedindung zutrifft.

{% include image.html image=page.image2 %}

## Schleife mit Laufvariable
Die dritte Schleife wird mithilfe einer Laufvariable umgesetzt, welche auch innerhalb des Programms eingesetzt werden kann. Zuerst wird eine Variable mit einem Startwert initialisiert und ein Maximalwert für sie festgelegt. Dann wird die Laufvariable nach jedem Durchgang um die angegebene Zahl erhöht. So kann für jeden Zustand der Laufvariable eine Anweisung festgelegt werden.

{% include image.html image=page.image3 %}

