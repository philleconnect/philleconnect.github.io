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

## Update

Ein Serverupdate ist denkbar einfach:

1. auf der Kommandozeile in den Ordner `ServerContainers` wechseln. Dies kann gerne auch per ssh aus der Ferne geschehen, z.B. mit dem freien ssh-client [PuTTY](https://de.wikipedia.org/wiki/PuTTY).
2. mit `git pull` die aktuellsten "Container-Baupläne" holen und schließlich
3. mit `sudo docker-compose up -d --build` die veränderten Server-Container neu erstellen und starten. (was viel schneller geht als bei der ersten Installation)

## Server stoppen und starten

Der Server kann wie jedes andere System heruntergefahren werden.

Nach dem Start des Betriebssystems können die Container aus dem Ordner _ServerContainers_ mit `sudo docker-compose up -d` gestartet werden. Wenn Docker automatisch mit dem Systemstart mit gestartet werden soll muss einmal auf dem Hostsystem `sudo systemctl enable docker.service` ausgeführt werden.

Sinnvoll ist es zuvor mit `sudo docker-compose down` sicher zu stellen dass alles zuvor korrekt angehalten wurde oder wird.

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
