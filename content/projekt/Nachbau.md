---
title: "Nachbau"
date: 2021-03-15T16:15:28+01:00
draft: false
---

### Anleitung zum Nachbauen

Unter der Seite "Einzelteile" findet man alle nötigen Komponenten die man für einen Nachbau benötigt.

#### Schritt 1

Alle Dateien die sich auf der Seite "3D-Druck" befinden, herunterladen und ausdrucken.


#### Schritt 2

Die Einzelteile wie folgt an den ESP anschließen.

##### DHT:

DA -> D5

GND -> GND

VCC -> 3V


##### BMP:

SCL -> D7

SCA -> D6

GND -> GND

Vin -> 3V

##### MQ5:

A0 -> A0

GND -> GND

VCC -> 3V

##### Feuer:

D0 -> D2

GND -> GND

VCC -> 3V


##### SDS011:

TXD -> D4

GND -> GND

5V -> 3V


#### Schritt 3

Unter der Seite "Code" findet man den Code der auf den ESP gespielt werden muss. Vorher sollten alle notwendigen Bibliotheken installiert werden. Im Anschluss muss ein Server bereitgestellt werden, der die Daten empfangen kann. Die URL des Servers dann im Code hinterlegen.
