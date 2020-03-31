---
title: "E-Technik"
date: 2019-11-11T11:46:30+01:00
draft: false
---

## Elektrotechnik Labor und Versuche

Im Labor für Elektrotechnik fanden verschiedene Versuche und Übungen statt um das Gelernte
bezüglich den Einheiten von Spannung, Strom und Widerstand zu vertiefen.

### Schritt 1: Widerstandsmessung

Nach einer kurzen Vorbesprechung mit entsprechenden Sicherheitsunterweisungen (Laborpartner nicht umbringen, etc.)
konnte mit den ersten Versuchen zur Widerstandsmessung begonnen werden. Als Erstes sollte nur mit Hilfe der Anzeigen
des Netzteils der Widerstand berechnet werden.

Das Netzteil liefert in diesem Versuch die Werte von Strom und Spannung, und durch Einsetzen der Werte in die passende Formel
kann der Widerstand des gegebenen Teils berechnet werden.

![Widerstandsmessung Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/etechniklabor/versuch1.jpg "Erster Versuch")

Nachdem mehrere Messwerte erhoben wurden konnte durch den Durchschnitt errechnet werden welchen Widerstand das Bauteil
ca. haben muss.

### Schritt 2: Widerstandsmessung mit Multimeter

Direkt im Anschluss folgte der zweite Versuch bei welchem wieder ein Widerstand gemessen werden sollte, diesmal aber unter
Verwendung eines [Multimeters](https://de.wikipedia.org/wiki/Multimeter "Wikipedia Multimeter"). Das Multimeter sollte dabei
helfen die Messgenauigkeit zu erhöhen und die im ersten Versuch festgestellten Werte zu verifizieren.

![Widerstandsmessung Multi Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/etechniklabor/versuch2.jpg "Zweiter Versuch")

Als Ergebnis der beiden Versuche lässt sich sagen, dass die Messung welche auf der Anzeige des Netzteils basiert
eine starke Abweichung hat. Dies liegt ua. auch daran, dass das Netzteil nur zwei Nachkommestellen anzeigen kann und
bei der Anzeige gerundet wird. Das Multimeter war hierbei deutlich genauer.

### Schritt 3: Widerstandsmessung mit Spannungsteiler

Im dritten Versuch wurde erneut ein Widerstand gemessen diesmal jedoch mit einem [Spannungsteiler](https://de.wikipedia.org/wiki/Spannungsteiler "Wikipedia Spannungsteiler"). Dieser Versuch war deshalb entscheidend weil man sich nicht mehr auf die
Strommessung verlassen musste. Der Versuch mit einem Spannungsteiler erfolgt mit zwei Widerständen, einem bekannten Widerstand und
dem zu messenden Widerstand. Um die Werte der Messung verwenden zu können muss eine Formel so umgestellt werden, dass sich der
Widerstandswert daraus berechnen lässt.

Leider kann ich hierzu kein Foto liefern dafür aber eines von einem brennenden Widerstand was auch sehr eindrucksvoll war.

![Burn Widerstand Burn Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/etechniklabor/burnit.png "Brennender Widerstand")

### Schritt 4: Arduino mit Heißleiter

In der finalen Phase des Labors hatten wir die Möglichkeit mit einem [Arduino Nano](https://store.arduino.cc/arduino-nano "Arduino Nano Website") zu arbeiten. Als Erstes mussten wir die Verbindungen an diesen Löten. Nachdem dies ohne größere Probleme
funktionierte konnte eine Schaltung auf einem Steckbrett gebaut werden welche den Arduino mit einem Heißleiter verbindet
und somit eine Temperaturmessung ermöglicht.

![arduino Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/etechniklabor/arduino.jpg "Arduino Nano")


![arduino schaltung Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/etechniklabor/schaltung.jpg "Arduino Temperatur Messschaltung")

Sobald durch die Arduino IDE das entsprechende Skript auf den Arduino geladen war konnte man in der Textausgabe der IDE beobachten
wie durch den Widerstand des Heißleiters die Raumtemperatur ermittelt wurde. Testen konnte man das System indem man den Heißleiter
von beiden Seiten mit einem Finger berührte oder ein Feuerzeug in die Nähe des Leiters hielt. Die Schwankung der Temperatur konnte
direkt danach auf dem Bildschirm abgelesen werden.

### Fazit

Ein sehr spannendes Labor indem man nicht nur bekannte Formeln mal in der Praxis anwenden kann sondern auch die Möglichkeit hat
Dinge auszuprobieren und zu lernen, die man vielleicht noch nie vorher getan hat zB. Löten. Im Rückblick gehe ich mit einer deutlich
höheren Kenntnis über elektrischen Strom und Schaltungen aus dem Labor und freue mich auf die kommenden Labore um noch mehr mit
dem Arduino und anderen Bauteilen zu experimentieren.  
