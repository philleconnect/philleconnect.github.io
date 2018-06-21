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
* Phase 2 Authentifizierung **GTC**
* Identität **persönlicher PhilleConnect Benutzername**
* Passwort **persönliches PhilleConnect Passwort**
* je nach System CA-Zertifikat immer akzeptieren/nicht prüfen/nicht angegeben oder vergleichbares auswählen

Im Einzelnen für die jeweiligen Betriebssysteme:

## Android

Einfach das WLan identifizieren und obige Werte an entsprechender Stelle eintragen.

## Windows (7)

Unter Windows 7 **muss** die Software des Geräteherstellers für die Verbindung mit dem WLan verwendet werden, da Microsoft die Unterstützung für GTC nicht eingebaut hat.

Hier ein Beispiel-Setup mit der Intel-Software auf einem Dell-Notebook:

![WLan verbinden]({{baseurl}}/assets/images/ScreenWLanWin7_1.png)

WLan mit der Hersteller-Software identifizieren...

![WLan ]({{baseurl}}/assets/images/ScreenWLanWin7_2.png)

... verbinden klicken ...

![WLan eintragungen]({{baseurl}}/assets/images/ScreenWLanWin7_3.png)

... `WPA2-TKIP` mit `PEAP` und `GTC` auswählen, Benutzername und Passwort eintragen ...

![WLan identifizieren]({{baseurl}}/assets/images/ScreenWLanWin7_4.png)

... und "Zertifikat validieren" deaktivieren.

(Da in einem internen Netz das Zertifikat nicht von einer CA validiert werden kann ist dies notwendig)
