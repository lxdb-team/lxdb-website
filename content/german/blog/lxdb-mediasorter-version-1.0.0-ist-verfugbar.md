---
author: "Denys Konovalov"
date: 2021-01-04T18:00:00Z
description: ""
image: "/images/lms/lms-ad.png"
image_webp: ""
title: "LXDB MediaSorter Version 1.0.0 ist verfügbar !"
---
## FMDS ist jetzt LXDB MediaSorter !

Das erste Programm von LXDB hieß FMDS und war ein Werkzeug zum Sortieren von Dateien.
Das vom Programmnamen aus nicht gleich verständlich war, wozu das Programm dient,
haben wir uns dazu entschlossen, dem Programm einen neuen Namen zu geben.

## Neuerungen in LMS v1.0.0

- lms ist jetzt ein Python-Paket und kann damit auf jedem Linux-System installiert werden.

### Neue Funktionen
> Neue Bildervorschau mit Zoom-Funktionalität
> Neue Videovorschau mit Unterstützung aller Videoformate
> Umschaltmöglichkeit zwischen einem rekursiven und einem lokalen Scan-Modus
> Geschwindigkeitsverbesserungen durch die Nutzung von subprocess statt os.system
  und einem BASH-Skript
> Eine Online-Dokumentation ist jetzt verfügbar

### Visuelle Veränderungen
> Neues Symbol
> Verbessertes Interface-Design
> Neuer "Über LXDB MediaSorter" Dialog
> Neues "Über Qt" Fenster
> Neuer Schließen-Button im Dateimenü
> Neuer "Dokumentation" Button im "Hilfe" Menü

### Interne Änderungen:
> Neuer Codestil: self.window.layout.element
> Interne Metadaten-Operationen(exiftool) werden nun mit einem subprocess Prozess realisiert
> Geschwindigkeitsverbesserungen
> Metadaten-Operationen sind ein einer extra Bibliothek kombiniert
> lms-cli ist jetzt ebenfalls ein Python-Skript
> lms iss jetzt eine Python-Bibliothek und der lms Skript startet nur die App()
Class aus der Bibliothek
