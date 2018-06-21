---
layout: page
title: Betrieb
permalink: /admins/RadiusServer
tags: Admins
lang: de
---

# **RADIUS**SERVER

## Was das ist

Ein Radiusserver hat sich als Standart gemausert um die Benutzerauthentifizierung für zum Beispiel WLan-Zugänge zu übernehmen.

PhilleConnect bietet als Optionalen Container einen Radiusserver an, der z.B. in (auch sehr günstigen) WLan-Access-Points eingerichtet werden kann. Benutzer können dann als WLan-Zugangskennung ihren PhilleConnect-Login verwenden.

## Wie einrichten?

Auf dem Server in dem Verzeichnis, in dem auch der Ordner `ServerContainers` liegt, einmal `git pull https://github.com/philleconnect/RadiusServer` ausführen.

Dann mit `cd RadiusServer` in das neue Verzeichnis wechseln und z.B. mit `nano settings.env` die Konfigurationsdatei mit eigenen Passwörtern ausstatten.

Schließlich mit `docker-compose up -d` den Container Bauen und starten - fertig.

## Und die Access-Points?

Hier eine Beispielkonfiguration:

![WLan identifizieren]({{baseurl}}/assets/images/ScreenWLanWin7_1.png)

Dabei ist die `172.16.0.102` durch die IP des eigenen PhilleConnect-Servers zu ersetzen.
