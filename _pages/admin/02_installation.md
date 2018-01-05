---
layout: page
title: Installation
permalink: /admin/Installation
tags: Admins
lang: de
---

# **INSTALLIEREN**

## Server

Die Installation des Servers ist in wenigen Schritten erledigt:

* Installiere auf einem Rechner [Ubuntu-Linux](https://ubuntu.com) (gerne als Server, ist aber eigentlich egal)
* Führe auf der Kommandozeile `sudo apt-get install docker docker-compose git` aus
* Führe auf der Kommandozeile `git clone http://github.com/philleconnect/ServerContainers/` aus.
* Trage in die `settings.env` an den jeweiligen Stellen eigene Passwörter ein.
* Wechsele in den Ordner `ServerContainers` mit `cd ServerContainers` und führe dort den Befehl `sudo docker-compose up -d` aus.
* Genieße einen Kaffee während du dem Rechner beim Arbeiten zusiehst.
* Wenn der Kaffee leer ist kannst du auf dem Rechner im Browser auf `http://localhost:84/setup/` gehen oder an einem anderen Rechner im gleichen Netzwerk auf `http://<serveradresse>:84/setup/`. Die Verbindung zur ipFire kann auch erstmal übersprungen und später eingerichtet werden, so dass nur der persönliche Admin-Zugang vergeben werden muss.
* Fertig.
* Die Administrationsoberfläche ist unter `http://<serveradresse>:84/ui/` oder per https (selbstsigniertes Zertifikat) unter `https://<serveradresse>:447/ui/` zu erreichen.

## Client

Dies ist so einfach, dass erst eine Anleitung folgt wenn wir bei der Stable-Version sind.

Einfach den [Client-Installer Downloaden](https://github.com/philleconnect/ClientSetup-Windows/blob/master/Installer/PhilleConnectSetup.exe) und auf dem Client-PC ausführen, den Rest erklärt der Installer.
