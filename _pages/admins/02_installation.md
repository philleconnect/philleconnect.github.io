---
layout: page
title: Installation
permalink: /admins/installation
tags: Admins
lang: de
---

# **INSTALLIEREN**

## **SERVER**INSTALLATION

Die Installation des Servers ist in wenigen Schritten erledigt:

* Installiere auf einem Rechner [Ubuntu-Linux](https://ubuntu.com) (gerne als Server, ist aber eigentlich egal)
* Führe auf der Kommandozeile `sudo apt-get install docker docker-compose git` aus
* Führe auf der Kommandozeile `git clone http://github.com/philleconnect/ServerContainers/` aus.
* Trage in die `settings.env` an den jeweiligen Stellen eigene Passwörter ein. Z.B. mit vim: `vim settings.env`
* Wechsele in den Ordner `ServerContainers' mit `cd ServerContainers' und führe dort den Befehl `sudo docker-compose up -d` aus.
* Genieße einen Kaffee während du dem Rechner beim Arbeiten zusiehst.
* Wenn der Kaffee leer ist kannst du auf dem Rechner im Browser zu `http://localhost:84/setup/` gehen. Die wesentlichen Daten sind bereits eingetragen, ausser die Verbindung zur ipFire, die erstmal nicht nötig ist.
* Fertig.

## **CLIENT**INSTALLATION

Dies ist so einfach, dass erst eine Anleitung folgt wenn wir bei der Stable-Version sind.

Einfach den [Client-Installer Downloaden](https://github.com/philleconnect/ClientSetup-Windows/blob/master/Installer/PhilleConnectSetup.exe) und auf dem Client-PC ausführen, den Rest erklärt der Installer.
