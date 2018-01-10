---
layout: page
title: Betrieb
permalink: /admins/Betrieb
tags: Admins
lang: de
---

# **BETRIEB**

## Alltag

Die alltäglichen Aufgaben des Admins lassen sich alle bequem von Jedem Rechner im Schulnetz ausführen. Die Weboberfläche kann erreicht werden unter

`http://<serveradresse>:84/ui/`

oder verschlüsselt (mit einem selbst-signierten Zertifikat, muss einmal im Browser bestätigt werden) unter

`http://<serveradresse>:447/ui/`

## Datensicherung

Es müssen nur von drei Orten Backups erstellt werden um das ganze Netzwerksystem nach vollständigem Verlust wieder her zu stellen:

Die Einstellungen in der `settings-yml` und gegebenenfalls weitere Anpassungen vor dem Bau der Containerlandschaft.

Nach der Inbetriebnahme sind alle backup-relevanten Serverdaten in dem Verzeichnis

`/var/lib/docker/volumes`

welches regelmäßig und nach wesentlichen Änderungen gesichert werden sollte.

Weiterhin natürlich die Samba-Laufwerke. Bei der Installation findet sich in dem `ServerContainers`-Ordner ein Unterordner `mount/` der diese in der Standarteinstellung beinhaltet.

Nach einem Totalausfall muss nur

* PhilleConnect neu Installiert werden
* Der Ordner `/var/lib/docker/volumes` wieder durch das Backup ersetzt werden
* Die Laufwerksdaten wieder an Ort und Stelle gebracht werden.
