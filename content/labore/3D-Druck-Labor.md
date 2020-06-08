---
title: "3D Druck"
date: 2020-02-03T12:51:14+01:00
draft: false
---

## Additive Fertigungsverfahren - Labor

Das finale Labor fand zum Thema Additive Fertigungsverfahren statt und beinhaltete das Erstellen einer Kabelhalterung
für den Schreibtisch. Vorgabe war es eine Halterung zu erstellen, welche sich seitlich an einem Schreibtisch anbringen
lässt, damit die eingehängten Kabel nicht vom Tisch auf den Boden fallen, sondern in der Halterung auf ihre nächste
Nutzung warten.

Des Weiteren galten Vorgaben bezüglich des Drucks. Der Druck durfte maximal 15 Minuten in Anspruch nehmen, und es musste
sich um ein von uns selbst designtes Objekt handeln. Es standen drei Drucker zur Verfügung, um also nicht in der Warteschleife
zu hängen, ohne zu wissen ob das eigene Objekt den Ansprüchen nun wirklich genügt habe ich mich bemüht so schnell wie möglich
einen Prototypen auszudrucken, an welchem ich mich dann orientieren konnte.

### Schritt 1: Messen

Zu Beginn ging es darum, die Abmessungen der Kabel sowie deren Stecker zu Erfassen und ein passendes Objekt zu entwerfen.
Die Messung ging anhand von [elektronischen Helfern](https://de.wikipedia.org/wiki/Messschieber "Wikipedia Messschieber") sehr schnell und man konnte direkt zum nächsten Schritt übergehen.

### Schritt 2: Design

Damit mindestens zwei Kabel in die Halterung passen muss die Plattform eine gewisse Breite erreichen, zudem sollten
Löcher für zwei Schrauben vorhanden sein, um das Endergebnis an einem Tisch festschrauben zu können. Um die Kabel nicht
von den Schrauben zu beeinträchtigen, habe ich die Löcher für die Schrauben horizontal platziert.

### Schritt 3: Modellieren

Jetzt sollte die Idee in ein 3D Modell umgewandelt werden. Genutzt wurde das Tool der Wahl, bei mir [Tinkercad](https://www.tinkercad.com/ "Tinkercad"), um aus verschiedenen Basisformen das eigene Modell zu erstellen.
Beim Modellieren werden mehrere verschiedene Grundformen wie zB. Würfel oder Zylinder zusammengesteckt und zu einem Objekt verbunden.
Es besteht zudem die Möglichkeit, Objekte vom eigentlichen Modell auszuschneiden um passende Formen zu erzeugen.
In meinem Beispiel habe ich mehrere Würfel genutzt, um aus meinem Objekt Teile auszuschneiden, damit die Arme entstehen welche
später die Kabel halten sollen. Auch hier spielt die Idee eine Rolle, dass die Druckzeit begrenzt ist, somit musste man alle Teile
sehr klein und möglichst dünn halten.

![Modellimage Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/3ddrucklabor/modell.png "Modellieren")

### Schritt 4: Slicen

Nachdem das Modell fertig war, ging es darum, das Ganze für den 3D Drucker lesbar zu machen und auch sicherzustellen, dass der
Druck wirklich nur 15 Minuten in Anspruch nimmt. Das werden sogenannte Slicer benutzt, ein Programm was ein Modell nimmt und
eine für den 3D Drucker lesbare .gcode Datei auswirft. Es gibt einem zudem die Möglichkeit jede einzelne Schicht des Drucks
vorher zu sehen und eventuelle Fehler zu erkennen. Die Einstellungen des Slicers beeinträchtigen dann die Druckqualität und
die nötige Zeit. Wichtige Einstellungen wären zB. die Schichthöhe und die Druckgeschwindigkeit. Unten sieht man Screenshots
aus dem Programm, das erste Bild ist das komplette Modell, beim Zweiten sieht man einen Querschnitt einer der unteren Schichten.

![Slicing Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/3ddrucklabor/slicing.png "Slicing")


![Schichten Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/3ddrucklabor/schicht.png "Schichten")

### Schritt 5: Drucken

Der letzte Schritt ist so unspektakulär wie spektakulär zugleich. Eigentlich nur SD Karte in den Drucker, Start drücken und fertig.
In den dann kommenden 15 Minuten könnte man sein Modell weiterentwickeln, quasi noch mal bei Schritt 3 einsteigen oder wenns ganz
mies läuft bei Schritt 2, man könnte auch den anderen helfen oder einfach was zu Trinken holen.
Trotzdem ist es sehr faszinierend dem 3D Drucker zuzusehen, wie er Schicht für Schicht das eigene Modell entstehen lässt.

Da ich zu Beginn ein sehr hohes Tempo hatte, um beim Drucker der Erste zu sein, hatte ich bereits erwartet, dass mein Modell einige
Macken haben würde. Nach einigen Iterationen war dann es dann allerdings so weit. Kein Wackeln mehr, die Kabel hielten solide in
der Vorrichtung und es machte auch einen einigermaßen stabilen Eindruck.

Unten sind einmal das finale Produkt mit einem Kabel zu sehen, sowie meine vorherigen Versuche.

![Finales Produkt 1 Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/3ddrucklabor/withcharger.jpg "finales Produkt")

![Finales Produkt 2 Image](https://raw.githubusercontent.com/Snoup97/swh-pkohler/master/static/img/3ddrucklabor/allprints.jpg "finales Produkt")
