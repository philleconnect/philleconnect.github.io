---
layout: page
title: NextCloud
permalink: /admins/NextCloud
tags: Admins
lang: de
---

# **NEXT**CLOUD

## Was das ist

Auch von zu Hause und eigenen Rechnern ist der Zugriff auf die persönlichen Laufwerke möglich. Die freie Software NextCloud, ein Fork der auch sehr bekannten OwnCloud, bietet für den Verzeichniszugriff eine moderne und einfache Oberfläche im Browser an.

Der PhilleConnect-NextCloud-Container integriert dabei den PhilleConnect-LDAP-Verzeichnisdiest, so dass der Zugriff für Anwender mit dem gleichen Benutzernamen und Passwort erfolgt wie die Anmeldung an den Schul-PCs oder, falls vorhanden, am Radius-Server für das Schulische WLan und alle anderen PhilleConnect-Dienste.

Darüber hinaus ist die freie Browser-basierte Office Suite OnlyOffice integriert, die das Bearbeiten von Office-Dokumenten wie Textverarbeitung- oder Präsentationen direkt im Browser ermöglicht, von jedem Endgerät - BYOD willkommen!

Und noch besser: Die Dateien können für andere Nutzer freigegeben werden und mit OnlyOffice sogar zeitgleich bearbeitet werden. Echte Kollaboration, wie es in die Schule gehört!

Die häuftigsten Zugriffe auf die Daten in der Schule erfolgen sicherlich von dort aus. Es macht also Sinn die Daten dort zu lagern, sogar ganz unabhängig von Datenschutzüberlegungen. Beim Zugriff von ausserhalb des Schulnetzes wird dann auch nur der gerenderte Ausschnitt aus dem gerade geöffneten Dokument übertragen. Das ermöglicht auch bei schmalbandigem Upload das Bearbeiten von aufgeblasenen Präsentationen.

Bitte Beachten: Wir setzten die Container bereits produktiv ein, nennen es aber vorsichtshalber noch Beta, ein paar Kleinigkeiten und möglicherweise weitere Vereinfachungen der Installation werden noch bis zum stable-Release vorgenommen.

## Wie einrichten?

Auf dem Server in dem Verzeichnis, in dem auch der Ordner `ServerContainers` liegt, einmal `git pull https://github.com/philleconnect/Nextcloud` ausführen.

Dann mit `cd Nextcloud` in das neue Verzeichnis wechseln und z.B. mit `nano settings.env` die Konfigurationsdatei mit eigenen Passwörtern und Einstellungen ausstatten.

Schließlich mit `docker-compose up -d` die Container Bauen und starten.

Für den Zugriff aus dem Internet muss schließlich noch der entsprechende Zugang eingerichtet werden. Dies hängt von der jeweiligen Situation ab (DSL, Kabel Glasfaser, Router, ...) und kann leider nicht automatisch ausgeführt werden. Nötig ist in der Regel:

* Ein DynDNS-Eintrag
* Port-Weiterleitungen
* Proxy-Server für verschlüsselten Zugriff
    * hierfür kann z.B. der PhilleConnect HttpLdapAuth-Container verwendet werden.
* Empfohlen: Verschlüsselter https-Zugriff mit z.B. Let's Encrypt zertifikaten (https ist für die OnlyOffice-Integration voreingestellt, bei unverschlüsseltem Zugriff z.B. für Testbetrieb über die Nextcloud-Admin-Oberfläche ändern!)

Etwas Erfahrung oder Recherche zum Thema "Eigene Dienste am Internetanschluss freigeben" ist hierfür leider unumgänglich.

In unserer Umgebung wird ein nginx-reverse-proxy (z.B. PhilleConnect HttpLdapAuth, zusätzlich mit Let's Encrypt Zertifikaten verrsorgt) mit folgender Konfiguration eingesetzt. Dabei hat der Host, auf dem PhilleConnect samt NextCloud läuft, die IP `172.16.0.100`, dies ist, genau wie die Domain, entsprechend dem eigenen Setup anzupassen.

```
# NextCloud:
server {
    listen 80;
    listen [::]:80;
    server_name cloud.domain.tld;
    return 301 https://cloud.domain.tld$request_uri;
}
server {
    listen 443 ssl;
    listen [::]:443 ssl;
    ssl_certificate /etc/letsencrypt/live/cloud.domain.tld/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/cloud.domain.tld/privkey.pem;
    server_name cloud.domain.tld;
    client_max_body_size 0;
    location / {
        client_max_body_size 0;
        proxy_set_header        Host                $host;
        proxy_set_header        X-Real-IP           $remote_addr;
        proxy_set_header        X-Forwarded-For     $proxy_add_x_forwarded_for;
        proxy_pass http://172.16.0.100:86/;
    }
}
# OnlyOffice:
server {
    listen 443 ssl;
    listen [::]:443 ssl;
    ssl_certificate /etc/letsencrypt/live/onlyoffice.domain.tld/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/onlyoffice.domain.tld/privkey.pem;
    server_name onlyoffice.domain.tld;
    location / {
        proxy_set_header        Host                $host;
        proxy_set_header        X-Forwarded-Proto   https;
        proxy_set_header        X-Real-IP           $remote_addr;
        proxy_set_header        X-Forwarded-For     $proxy_add_x_forwarded_for;
        proxy_pass http://172.16.0.100:82/;
    }
}
```

TODO: Teile der Konfiguration wird möglicherweise bis zum stable-Release in PhilleConnect Nextcloud integriert.
