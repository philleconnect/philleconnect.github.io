---
layout: page
title: WLan
permalink: /anwender/WLan
tags: Anwender
lang: de
---

# **WLAN**VERBINDEN

Sofern die WLan-Authentifizierung mit den PhilleConnect-Logins eingerichtet ist sind folgende Einstellungen notwendig, um sich mit mit dem Netzwerk zu verginden:

* Authentifizierungstyp **WPA2 Enterprise**
* EAP-Methode **PEAP**
* Falls Einstellung möglich: Phase 2 Authentifizierung **MS-CHAPv2** (oder wahlweise GTC)
* Identität **persönlicher PhilleConnect Benutzername**
* Passwort **persönliches PhilleConnect Passwort**
* je nach System **CA-Zertifikat immer akzeptieren/nicht prüfen/nicht angegeben** oder vergleichbares auswählen

Im Einzelnen für die jeweiligen Betriebssysteme:

## Android

Einfach das WLan identifizieren, verbinden und im Verbindungsdialog obige Werte eintragen.

![WLan mit Android verbinden]({{baseurl}}/assets/images/ScreenWLanAndroid.png)

## Windows 10

Windows 10 fragt bei der Verbindung ob dem Zertifikat vertraut wird, dies muss bestätigt werden.

Die Frage nach dem Benutzernamen und Passwort erscheint beim Verbinden.

## macOS

Es muss nur der Benutzername und das Kennwort eintragen werden und die bei der Nachfrage nach dem Zertifikat "Vertrauen" ausgewählt werden.

## Windows 7

Leider kann Windows 7 noch nicht die Konfiguration automatisch erkennen.

Hier muss insbesondere manuell eingestellt werden, dass das Zertifikat nicht geprüft werden soll.

Dazu:

* Bei der Anzeige der Drahtlosnetzwerke auf "Netzwerk- und Freigabecenter" klicken
* Links auf "Drahtlosnetzwerke verwalten"
* "Hinzufügen"
* "manuell erstellen"
* Nun den Netzwerknamen (SSID) eintragen, den Sicherheitstyp "WPA2-Enterprise" und den Verschlüsselungstyp "TKIP"
* "Verbindungseinstellungen andern" anklicken
* "Einstellungen" -> "Serverzertifikat überprüfen" deaktivieren
* In dem gleichen Fenster !Authentifizierungsmethode" "Gesichertes Kennwort (EAP-MSCHAP v2)"
* Nach dem Klick auf "Konfigurieren..." noch das Häkchen in dem Eigenschaftenfenster entfernen
* Zu guter Letzt nach dem Klick auf "Erweiterte Einstellungen" den Authentifizierungsmodus auf "Benutzerauthentifizierung" stellen

Nun wird beim Verbinden mit dem WLan ein Dialogfenster angezeigt, in dem der Benutzername und das Passwort abgefragt werden.
