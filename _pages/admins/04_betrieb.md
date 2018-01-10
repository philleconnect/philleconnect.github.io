---
layout: page
title: Betrieb
permalink: /admins/Betrieb
tags: Admins
lang: de
---

# **BETRIEB**

## Alltag

Die alltäglichen Aufgaben des Admins lassen sich alle bequem von jedem Rechner im Schulnetz ausführen. Die Weboberfläche kann erreicht werden unter

`http://<serveradresse>:84/ui/`

oder verschlüsselt (mit einem selbst-signierten Zertifikat, muss einmal im Browser bestätigt werden) unter

`http://<serveradresse>:447/ui/`

## Datensicherung

Es müssen nur von drei Orten Backups erstellt werden um das ganze Netzwerksystem nach vollständigem Verlust wieder herzustellen:

1. Die Einstellungen in der `settings.yml`

2. Nach der Inbetriebnahme sind alle backup-relevanten Serverdaten (LDAP-Datenbank, PC-Datenbank, ...) in dem Verzeichnis
    
    `/var/lib/docker/volumes`
    
    welches regelmäßig und nach wesentlichen Änderungen gesichert werden sollte.

3. Weiterhin müssen natürlich die Samba-Laufwerke mit den Nutzerdaten gesichert werden. Bei der Installation findet sich in dem _ServerContainers_-Ordner ein Unterordner `mount/` der diese in der Standardeinstellung beinhaltet.



### Nach einem Totalausfall

muss nur

1. PhilleConnect neu installiert und die Einstellungen aus der `settings.env`-Datei übernommen werden,
2. der Ordner `/var/lib/docker/volumes` wieder durch das Backup ersetzt
3. und die Laufwerksdaten wieder an Ort und Stelle gebracht werden.

## Update

Um den Server auf die neueste stabile Version zu updaten müssen auf der Kommandozeile in dem Ordner `ServerContainers`

1. mit `sudo docker-compose down` die Server-Container angehalten werden
2. mit `git pull` die aktuellsten "Container-Baupläne" geholt werden und schließlich
3. mit `sudo docker-compose up -d --build` die Server-Container neu erstellt und gestartet werden. (was viel schneller geht als bei der ersten Installation)

## Server stoppen und starten

Der Server kann wie jedes andere System heruntergefahren werden.

Nach dem Start des Betriebssystems können die Container aus dem Ordner _ServerContainers_ mit `sudo docker-compose up -d` gestartet werden.

Entsprechend können diese auch mit `sudo docker-compose down` angehalten werden.
