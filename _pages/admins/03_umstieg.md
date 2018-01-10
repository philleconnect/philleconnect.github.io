---
layout: page
title: Umstieg
permalink: /admins/Umstieg
tags: Admins
lang: de
---

# **UMSTIEG**

oder

# INTEGRIEREN IN DEN BESTAND

PhilleConnect kann parallel zu bestehenden Schulnetzwerklösungen betrieben werden, um einen sanften Übergang zur Freiheit zu schaffen ;-)

**Grundlegende Kenntnisse im Umgang mit Linux auf der Kommandozeile sind dabei zu empfehlen!**

Aus dem vorhandenen System müssen dazu entweder die Benutzerdaten exportiert werden, die dann als CSV-Datei von PhilleConnect eingelesen werden kann (falls vorhanden einschließlich Klartext-Passwörtern), oder die Benutzer werden anhand einer vorhandenen Nutzerliste neu angelegt, erhalten dann natürlich neue Passwörter.

Beim Import können Passworter aus der CSV-Datei übernommen werden, diese können zum Beispiel im Tabellenkalkulationsprogramm erzeugt werden.

Die vorhandenen Laufwerks-Daten können auf dem Server-Rechner in den Ordner `ServerContainers/mount/` (vgl. [Installation](/admin/Installation)) eingebunden werden. Details dazu liefert zum Beispiel eine Internetsuche mit den Stichworten `mount fstab network`.

Bei mir (Umstieg von LANiS) lösen das Problem ein paar Einträge nach dem folgenden Muster in der Datei `/etc/fstab` auf dem Server-Rechner:

    //172.16.0.1/D$/LANiSData/Exchange/School/ /home/serveruser/PhilleConnect/mount/samba/schoolExchange cifs credentials=/root/.smbcredentials,iocharset=utf8,rw,dir_mode=0777,file_mode=0777,user,auto,uid=serveruser 0 0

wobei in `/root/.smbcredentials` noch eine Datei mit etwa diesem Inhalt liegt:

```
username=MeinFreigabeBenutzername
password=MeinServerPasswort
domain=MeineSchule.local
```

Sorry, aber genauere Informationen können wir hier leider nicht wirklich geben, da es vom jeweiligen Schulnetz abhängt. Wir hoffen es reicht für die Idee und die wesentlichen Schuchwörter. Für das Hessische System "LANiS" kann es daber direkt zu verwendet werden.

Viel Erfolg!
