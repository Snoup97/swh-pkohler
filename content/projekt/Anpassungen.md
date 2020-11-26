---
title: "Anpassungen"
date: 2020-11-26T08:06:20+01:00
draft: false
---

Nicht alles läuft immer wie geplant, und da ist dieses Projekt keine Ausnahme.
Aus verschiedenen Gründen musste ich einige Anpassungen am eigentlichen Plan machen.

### Mobile-App

Auf Grund des Aufwands eine Mobile App zu programmieren und diese dann über die API an die Station anzubinden, habe ich mich entschieden diesen Bereich etwas abzuändern.
Statt einer App fürs Handy, habe ich eine kleine Web-App gebastelt und auf einen Server gelegt. Somit kann die Station, sobald sie eine Internetverbindung hat ihre Daten an den Server schicken. Die Web-App bereitet die Daten etwas auf und stellt deren Verlauf dar.
Die Web-App kann auch Daten von mehreren Stationen empfangen und darstellen. Dazu bräuchte man aber mehrere baugleiche Stationen.

### Display an der Station

Der Plan sah vor ein 1,3 Zoll großes OLED Display an die Station anzuschließen um deren Daten auch direkt dort anzeigen zu können. Leider war das Display defekt und konnte nur die ersten Pixelreihen korrekt anzeigen der Rest war eine Mischung aus hellen und dunklen Pixeln, welche sich nicht zurücksetzen ließen.
Leider hatte ich kein Ersatzdisplay, und musste diese Idee deshalb streichen.

### SDS011

Hoffentlich nur ein temporärer Eintrag, aber im Moment bereitet der SDS011 Feinstaubsensor große Probleme, da er sich nicht anschließen lässt. Trotz vieler Tutorials im Netz ist es mir für den Moment nicht möglich die Daten vom Sensor korrekt auszulesen.
