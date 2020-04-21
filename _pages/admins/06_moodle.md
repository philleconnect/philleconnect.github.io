---
layout: page
title: moodle
permalink: /admins/moodle
tags: Admins
lang: de
---

# **moodle**

## moodle-Container

Die, zumindest in Deutschland, am weitesten verbreitete eLearning-Plattform lässt sich in wenigen Minuten in PhilleConnect integrieren. Lehrende können dabei selbständig Kurse erstellen und diese verwalten, Lernende haben wie gewohnt mit den gleichen Zugangsdaten direkt Zugriff darauf.

## Wie einrichten?

### Setup des Containers

Auf dem Server in dem Verzeichnis, in dem auch der Ordner `ServerContainers` liegt, einmal `git pull https://github.com/philleconnect/moodle` ausführen.

Anschließend mit `git submodule update --init` das aktuelle Moodle von github holen und mit `git submodule foreach git checkout v3.8.2` die gewünschte Version auswählen.

Dann mit `cd moodle` in das neue Verzeichnis wechseln, mit `cp settings.env.default settings.env` eine produktiv-Kopie der Konfiguration erstellen und z.B. mit `nano settings.env` die Konfigurationsdatei mit eigenen Passwörtern ausstatten. Dabei kann die moodle-Installation auf einem anderen System als der PhilleConnect-Server laufen.

Schließlich mit `docker-compose up -d` den Container Bauen und starten - fertig. Dabei sind ein paar Minuten Geduld nötig, moodle braucht beim ersten Start eine Weile zur Initialisierung.

Ggf. sollte das 

### Verbindung zum LDAP herstellen

Die Verbindung zum LDAP muss manuell über die grafische Benutzeroberfläche hergestellt werden, es sind nur folgende Eintragungen nätig:

- als admin anmelden
- Klick auf 'Website-Administration' > 'Plugins', dort auf 'LDAP-Server'
- Für die LDAP-url die IP-Adresse des PhilleConnect-Servers eintragen
- Die Eintragung des LDAP-bind ist nicht nötig, das LDAP-Passwort muss nicht an moodle herausgegeben werden.
- in 'user lookup' select the `rfc2307` for OpenLDAP
- bei `memberattribute` (kleiner grauer text, der Einheitlichkeit hier als offizieller Bezeichner übernommen, bedarfsweise suchen) `memberuid` eintragen, damit die automatische Rollenvergaben funktioniert
- bei `context` `ou=users,dc=ldap,dc=philleconnect` eintragen bei einer PhilleConnect-Standardinstallation
- als `passtype` `MD5` wählen
- für `removeuser` empfehlen wir `delete`
- und bei `coursecreatorcontext` muss `cn=teachers,ou=groups,dc=ldap,dc=schoolconnect` eingetragen werden damit Lehrer Kurse anlegen dürfen
