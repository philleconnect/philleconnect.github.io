---
layout: page
title: Installation
permalink: /admins/Installation
tags: Admins
lang: de
---

# **INSTALLIEREN**

## Server

Die Installation des Servers im Detail. Für ein Testsystem können auch einzelne Punkte übersprungen werden.

1. Installiere auf dem Server **[Ubuntu-Linux](https://ubuntu.com)** (gerne als Server, ist aber eigentlich egal).
    
    Nur für Profis: Dies kann auch in einer Virtuellen Maschiene z.B. auf einem [Proxmox](https://www.proxmox.com){:target="_blank"}-Server geschehen, nur nicht in einem Linux-Container.
    
2. Sorge dafür, dass dieser Rechner **immer die gleiche IP-Adresse** bekommt 
    1. z.B. im Router entsprechend einrichten 
    2. oder eine statische IP-Adresse vergeben
3. Führe auf der Kommandozeile `sudo apt-get update && sudo apt-get install docker docker-compose git` aus.
4. Führe auf der Kommandozeile `git clone http://github.com/philleconnect/ServerContainers/` aus.
5. Trage in die `settings.env` (mit Texteditor bearbeiten) mindestens in den ersten beiden Optionen eigene Passwörter ein und unter der dritten Option die dauerhafte IP-Adresse des Servers.
6. Wechsle mit `cd ServerContainers` in den Ordner mit den "Container-Bauplänen" und führe dort den Befehl `sudo docker-compose up -d` aus um diese zu erzeugen.
    1. Zeit zum Kaffee kochen
7. Gehe im Browser auf `http://localhost:84/setup/` oder an einem anderen Rechner im gleichen Netzwerk auf `http://<server-ip>:84/setup/`. Die Verbindung zur ipFire kann auch erstmal übersprungen und später eingerichtet werden, so dass nur der persönliche Admin-Zugang vergeben werden muss.
8. Fertig.
9. Die Administrationsoberfläche ist unter `http://<serveradresse>:84/ui/` oder per https (selbstsigniertes Zertifikat) unter `https://<serveradresse>:447/ui/` zu erreichen.

*Tipp:* Um bei jedem Systemstart automatisch Docker mit zu starten muss in neueren Ubuntu-Versionen einmal `sudo systemctl enable docker.service` ausgeführt werden.

## ipFire

Für die Internetsperre ist ein [IPFire-Router](https://www.ipfire.org/) nötig, der separat installiert werden muss. Wird die Internetsperre von PhilleConnect (erstmal) nicht benötigt tut auch jeder andere Router.

## Nutzer hinzufügen

Die einfachste Möglichkeit, viele Nutzer gleichzeitig hinzu zu fügen, ist der Import mit Hilfe einer CSV-Datei, die mit jedem Tabellenkalkulationsprogramm wie LibreOffice Calc oder MS Excel erstellt werden kann.

Die Import-Tabelle sollte den Vornamen, den Nachnamen, das Geburtsdatum und die Klasse (für Lehrer hier z.B. "Lehrer" eintragen) beinhalten.

Auch können hier Passworte z.B. aus dem alten Schulnetzwerksystem oder aus einem Passwortgenerator enthalten sein.

Beim Speichern/Exportieren einfach für das Dateiformat "Text/CSV" oder gleichwertiges auswählen.

Ggf. wird beim speichern noch nachgefragt welche Trennzeichen verwendet werden sollen. Ein `,` tut als Feldtrenner seine Dienste, ein Texttrenner (bei LibreOffice standardmässig `"`) sollte _nicht_ verwendet werden.

Die exportierte CSV-Datei kann dann mit einem Texteditor geöffnet und per copy-paste im CSV-Importer der Admin-Oberfläche hinzugefügt werden.

Alles weitere ist auf der Seite selbst erklärt.

## Konfigurationsprofile

Die Konfigurationsprofile legen zum Beispiel fest, welche Netzlaufwerke für eine Gruppe von Rechnern nach der Anmeldung eingebunden werden sollen. So können z.B. für unterschiedliche Räume unterschiedliche Tauschlaufwerke eingerichtet werden. Hat ein Konfigurationsprofil den gleichen Namen wie der Raum, für den später ein Client registriert wird, so wird der Client automatisch diesem Profil zugewiesen.

**Wichtig:** Die _SMB Server URL_ sollte in der normalen Installation die IP-Adresse des Servers beinhalten (prinzipiell ermöglicht PhilleConnect auch den Zugriff auf externe Samba-Server)

Der Servicemode schaltet für alle Rechner, denen das Profil zugewiesen ist, den Login aus.

## Client

In der Admin-Oberfläche findet sich unter _clientinstallation_ ein Link zum Download des aktuellen Installers, welcher z.B. auf einem USB-Stick gespeichert werden kann.

In dem gleichen Verzeichnis sollte auch die Konfigurationsdatei liegen die ebenfalls auf der Seite erstellt werden kann.

**Wichtig:** Achten Sie darauf, dass vor dem Klick auf _Installationsdatei erstellen_ die Parameter, **insbesondere die Server-URL (=IP-Adresse des Servers) ,ot port 447** korrekt eingetragen ist!

Nach der Installation des Clients, die durch den Installer erklärt wird, ist dem PC noch in der Admin-Oberfläche unter _Rechnerverwaltung_ ein Konfigurationsprofil zu zu ordnen.
