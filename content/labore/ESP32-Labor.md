---
title: "ESP32"
date: 2019-12-04T17:22:14+01:00
draft: false
---

## ESP32 Labor

Im Anschluss an das Arduino Labor wurde mit dem ESP32 das Board durch eines mit deutlich höherer Leistungsfähigkeit und
Möglichkeiten ausgetauscht. Mit dem ESP ist es ua. möglich eine Verbindung über Wlan herzustellen sowie selbst einen Webserver
zu hosten. Mit dem direkt auf das Board aufgestecken Display wird eine weitere Ausgabe- und Interaktionsmöglichkeit gegeben.

### Schritt 1: Bild auf Display ausgeben

Als erster Schritt wurde das aufgesteckte Display verwendet, um ein gegebenes Bild auszugeben. Das Bild war hierbei in einem
Array gespeichert, welches die Helligkeit des jeweiligen Pixels enthält.

![Array zu Bild](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/esplabor/1.jpg "Darstellung eines Bildes")

### Schritt 2: Ultraschall Entfernungsmessung

Um das System mit einer weiteren Interaktionsmöglichkeit zu erweitern, wurde eine Ultraschall-Entfernungsmessung angeschlossen.
Diese ermöglicht, über ihre Sensoren eine geringe Entfernung zu messen und an das Board zu übertragen.

![Anschluss Entfernungsmessung](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/esplabor/2.jpg "Anschluss einer Entfernungsmessung")

### Schritt 3: Webserver

Um die Möglichkeiten des Boards endlich zu nutzen, wird in diesem Schritt ein Webserver mit dem ESP gehostet. Hierzu erstellt der
ESP ein eigenes Netzwerk mit Passwort, und ermöglicht jedem der sich in diesem Netzwerk anmeldet die Seite in einem Webbrowser zu laden.

![Webserver](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/esplabor/3.jpg "Erstellen des Webservers")

### Schritt 4: Daten auf Website ausgeben

Um in einem finalen Schritt die Komponenten zusammenzuführen, wurde die Seite, welche vom Server ausgegeben wird mit einer Anzeige
erweitert, welche die gemessene Entfernung darstellt. Um die Daten immer aktuell zu halten, lädt sich die Seite jede Sekunde selbst neu.
Auch wenn dies in einem wirklichen System nicht vorkommen sollte, erfüllt es in diesem Fall den Zweck der Darstellung einer Zahl.

![Kombination](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/esplabor/4.jpg "Kombination der Komponenten")

### Fazit

Die Möglichkeiten eines ESP Boards gehen natürlich noch viel weiter als diesen Anwendungsfall. Trotzdem konnte man schön sehen, was alles möglich ist und die Komplexität solcher Systeme kann stark ansteigen. Da ESP Boards und Zubehör günstig im Internet zu
erwerben sind, kann ich jedem Interessierten nur raten, es einfach mal auszuprobieren. Dafür muss man ja schließlich nicht studiert haben ;).
