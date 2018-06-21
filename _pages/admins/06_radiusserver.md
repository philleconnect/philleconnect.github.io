---
layout: page
title: RadiusServer
permalink: /admins/RadiusServer
tags: Admins
lang: de
---

# **RADIUS**SERVER

## Was das ist

Ein Radiusserver hat sich als Standard gemausert um die Benutzerauthentifizierung für zum Beispiel WLan-Zugänge zu übernehmen.

PhilleConnect bietet als Optionalen Container einen Radiusserver an, der z.B. in (auch sehr günstigen) WLan-Access-Points eingerichtet werden kann. Benutzer können dann als WLan-Zugangskennung ihren PhilleConnect-Login verwenden.

## Wie einrichten?

Auf dem Server in dem Verzeichnis, in dem auch der Ordner `ServerContainers` liegt, einmal `git pull https://github.com/philleconnect/RadiusServer` ausführen.

Dann mit `cd RadiusServer` in das neue Verzeichnis wechseln und z.B. mit `nano settings.env` die Konfigurationsdatei mit eigenen Passwörtern ausstatten.

Schließlich mit `docker-compose up -d` den Container Bauen und starten - fertig.

## Und die Access-Points?

Hier eine Beispielkonfiguration:

![WLan identifizieren]({{baseurl}}/assets/images/ScreenRadiusAccessPoint.png)

Dabei ist die `172.16.0.102` durch die IP des eigenen PhilleConnect-Servers zu ersetzen.

## Unterscheidung zwischen Lehrern und Schülern

In der `settings.env`-datei findet sich eine Einstellung ob der Server nur Lehrer oder alle Benutzer zulassen soll.

Wird beides im Schulnetz benötigt, z.B. weil die Access-Points, die auch für Schüler sind, ein isoliertes Netz zur Verfügung stellen, so können problemlos zwei Container parallel gestartet werden.

Für den zweiten Container müssen dann nur in der `docker-compose.yml` andere Ports als öffentliche Ports angegeben werden wenn es auf dem gleichen Server läuft. Je nach eingestelltem Port im Access-Point werden dann nur Lehrer oder auch Schüler zugelassen.
