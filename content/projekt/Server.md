---
title: "Server"
date: 2021-03-16T20:43:30+01:00
draft: false
---


### Die Webapplikation

Jedes mal wenn die Station Daten verschickt müssen diese auch irgendwo empfangen und verarbeitet werden. Für diesen Zweck habe ich eine Web-App aufgesetzt, welche sich darum kümmert.

Die App basiert dabei auf dem Laravel Framework für PHP und läuft auf einem eigenständigen Server.

Die App empfängt über ihre API die Daten der Station und speichert sie in einer MySql Datenbank. Damit die Station eindeutig zugeordnet werden kann, ist im Code der Station ein Name hinterlegt, welcher mitgesendet wird. Somit kann die App auch Daten mehrerer Stationen empfangen.

Der Code befindet sich [hier](https://github.com/Snoup97/AirQualityStation "Server-App").

#### Übersicht der Stationen

![Dashboard Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/webapp/home.png "Dashboard")

#### Liste aller Messungen

![Messungen Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/webapp/messungen.png "Messungen Liste")

#### Ansicht einer Messstation

![Station Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/webapp/station.png "Station Liste")
