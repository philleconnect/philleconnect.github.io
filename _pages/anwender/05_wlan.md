---
layout: page
title: WLan
permalink: /anwender/WLan
tags: Anwender
lang: de
---

# **WLAN**VERBINDEN

Sofern die WLan-Authentifizierung mit den PhilleConnect-Logins eingerichtet ist sind folgende Einstellungen notwendig, um sich mit mit dem Netzwerk zu verbinden:

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

Leider kann Windows 7 noch nicht die Konfiguration automatisch erkennen, so dass einmalig **zwei Minuten Handarbeit** nötig sind.

Im Einzelnen:

* Bei der Anzeige der Drahtlosnetzwerke auf "Netzwerk- und Freigabecenter" klicken

	![WLan mit Android verbinden]({{baseurl}}/assets/images/ScreenWLanWin7_1.png)
	
* Links auf "Drahtlosnetzwerke verwalten"

	![WLan mit Android verbinden]({{baseurl}}/assets/images/ScreenWLanWin7_2.png)
	
* "Hinzufügen"

	![WLan mit Android verbinden]({{baseurl}}/assets/images/ScreenWLanWin7_3.png)
	
* "manuell erstellen"

	![WLan mit Android verbinden]({{baseurl}}/assets/images/ScreenWLanWin7_4.png)
	
* Nun den Netzwerknamen (SSID) eintragen, den Sicherheitstyp "WPA2-Enterprise" und den Verschlüsselungstyp "TKIP"

	![WLan mit Android verbinden]({{baseurl}}/assets/images/ScreenWLanWin7_5.png)
	
* "Verbindungseinstellungen andern" anklicken

	![WLan mit Windows 7 verbinden]({{baseurl}}/assets/images/ScreenWLanWin7_6.png)
	
* "Einstellungen" -> "Serverzertifikat überprüfen" deaktivieren

	![WLan mit Windows 7 verbinden]({{baseurl}}/assets/images/ScreenWLanWin7_7.png)
	
	![WLan mit Windows 7 verbinden]({{baseurl}}/assets/images/ScreenWLanWin7_8.png)
	
* In dem gleichen Fenster "Authentifizierungsmethode" > "Gesichertes Kennwort (EAP-MSCHAP v2)"

* Nach dem Klick auf "Konfigurieren..." noch das Häkchen in dem Eigenschaftenfenster entfernen

	![WLan mit Windows 7 verbinden]({{baseurl}}/assets/images/ScreenWLanWin7_9.png)
	
* Zu guter Letzt nach dem Klick auf "Erweiterte Einstellungen" den Authentifizierungsmodus auf "Benutzerauthentifizierung" stellen

	![WLan mit Windows 7 verbinden]({{baseurl}}/assets/images/ScreenWLanWin7_10.png)
	
	![WLan mit Windows 7 verbinden]({{baseurl}}/assets/images/ScreenWLanWin7_11.png)
	

Nun wird beim Verbinden mit dem WLan ein Dialogfenster angezeigt, in dem der Benutzername und das Passwort abgefragt werden.

![WLan mit Windows 7 verbinden]({{baseurl}}/assets/images/ScreenWLanWin7_12.png)
