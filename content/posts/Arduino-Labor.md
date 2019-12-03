---
title: "Arduino Labor"
date: 2019-11-27T12:19:21+01:00
draft: false
---

### Arduino Labor

Im Rahmen des Arduino Labors wurde ein Arduino Uno verwendet um die Werte mehrerer Sensoren auszulesen und diese
nach Möglichkeit dem Nutzer zu präsentieren. Hierzu standen ein Starter-Kit mit dem Arduino Uno sowie eine Sammlung
aus 37 Sensoren zur Verfügung.

Im ersten Abschnitt wurde der [Aruino](https://en.wikipedia.org/wiki/Arduino_Uno "Wikipedia Arduini Uno") mit einem
Temperatursensor verbunden und die Werte wurden über eine Konsole am Laptop ausgegeben. Der DHT11 Sensor kann hierbei
die Temperatur sowie die Luftfeuchtigkeit messen und ausgeben.

![UnoTemp1 Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/arduinolabor/versuch1.jpg "Erster Versuch")

Um dem Aufbau mehr Interaktion zu verleihen und um die Werte auf einem externen Display darstellbar zu machen wurde im nächsten
Schritt ein Display mit 4 Stellen angebaut. Das Display zeigt in einem regelmäßigen Wechsel die zuletzt gemessene Temperatur und
Luftfeuchtigkeit.

![UnoTemp2 Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/arduinolabor/versuch2.jpg "Zweiter Versuch")

Um einen weiteren Signalgeber zu verbauen und somit noch mehr mit dem Nutzer zu interagieren wurde ein Piepser verbaut der mit einem
kurzen Ton signalisiert wann eine Messung stattfindet. Der Ton wird angeschaltet kurz bevor die Messung beginnt und deaktiviert sobald
diese abgeschlossen ist.

![UnoTemp3 Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/arduinolabor/versuch3.jpg "Dritter Versuch")

Im finalen Schritt wurde ein Ultraschall-Entfernungsmesser angebaut, welcher die Entfernung bis auf eine gewisse Distanz messen und
ausgeben kann. Die gemessene Entfernung wurde hierbei nur auf einer Konsole am angeschlossenen Laptop ausgegeben.

Mit der entsprechenden Software kann nun der Aufbau soweit erweitert werden, dass der Entfernungsmesser die Distanz zum nächsten
Objekt vor der Messtation misst und sobald diese eine Grenze unterschreitet kann geschlussfolgert werden, dass sich ein Nutzer
vor der Station befindet. Daraufhin wird ein Ton ausgegeben und es findet eine Messung statt, die Werte werden anschließend auf
dem Display ausgegeben. 

![UnoTemp4 Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/arduinolabor/versuch4.jpg "Vierter Versuch")
