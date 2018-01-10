---
layout: page
title: ProblemLösungen
permalink: /admins/ProblemLoesungen
tags: Admins
lang: de
---

# **PROBLEM**LÖSUNGEN

(Diese Seite wird ergänzt wenn uns relevante Probleme zugetragen werden)

Sie können **mit `Strg` + `F` diese Seite durchsuchen**!

### Nachricht "**Konfigurationsfehler. Programm wird beendet.**" beim Login oder Teacher/Drive-Client
Prüfen Sie folgendes:
* Ist der Rechner in der Administrationsoberfläche registriert (mit der richtigen MAC-Adresse)?
* Ist ihm ein Konfigurationsprofil zugewiesen?
* Ist das Konfigurationsprofil korrekt, z.B. beim Samba-Server die richtige Adresse eingetragen und konfigurierte Laufwerke existieren im Samba-Server?
* Ist die Konfigurationsdatei "pcconfig.jkm" korrekt, insbesondere das Globale Passwort darin? Die Datei kann mit einem Texteditor geöffnet und mit der Grundkonfiguration in der Adminoberfläche verglichen werden.

### Nachricht "**Netzwerkfehler. Programm wird beendet.**" beim Login oder Teacher/Drive-Client
* Ist das Netzwerkkabel verbunden?
* Bekommt der Rechner eine passende IP-Adresse?
* Funktionieren andere Netzwerkaufgaben, z.B. der direkte Zugriff auf den Samba-Server mit `\\<ip-des-Servers>\`?
* Ist in der Konfigurationsdatei `C:\Programme\PhilleConnect\pcconfig.jkm` (Editierbar mit einem Texteditor) unter `server=` die richtige Adresse des Servers angegeben?

### Die **Benutzerliste beim Login ist leer**
In der Regel sollte der Login trotzdem möglich sein.

Die Ursache für die Leere Liste können ein falsches Konfigurationsprofil oder schlicht Netzwerkfehler/Timeouts sein. Bei letzterem sollte die Liste nach einem Neustart wieder voll sein.

Oder: Siehe nächster Punkt

### In der Administrationsoberfläche ist die **Liste der Accounts leer**

Vermutlich wurden die Container nicht sauber mit `sudo docker-compose down` beendet. Führen Sie diesen Befehl in dem Ordner _ServerContainers_ aus und starten Sie danach mit `sudo docker-compose up -d` die Container neu.

### Der **Login-Bildschirm ist leer und reagiert nicht**
Höchst wahrscheinlich liegt ein Konfigurations- oder Netzwerkfehler vor, der nicht automatisch erkannt werden konnte.

* Wenn Sie den Client mit einer Konfiguration "Rechner offline freigeben" (Standarteinstellung) installiert haben, können Sie den Login-Bildschirm umgehen indem Sie den Rechner starten wenn er vom Netzwerk getrennt ist.
* Wenn Sie für den Client die Offline-Freigabe nicht aktiviert haben, können Sie den Rechner im abgesicherten Modus starten.

Prüfen Sie dann ob der Rechner eine korrekte IP-Adresse zugewiesen bekommt und er den Server erreichen kann.

### Fehlt ein Fehler?

Schreiben Sie uns was fehlt in einer aussagekräftigen eMail an `it [ät] polarwinkel [punkt] de` !
