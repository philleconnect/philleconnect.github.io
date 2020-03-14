---
layout: default
permalink: /index.html
---

# **PHILLE**CONNECT

## Schul-IT der nächsten Generation: PhilleConnect ist eine moderne, modulare und anpassbare OpenSource Schulnetzwerk-Lösung

<div class="swiper-container">
    <!-- Additional required wrapper -->
    <div class="swiper-wrapper">
        <!-- Slides -->
        <div class="swiper-slide"><img src="{{baseurl}}/assets/images/architecture.png" width="800px" /></div>
        <div class="swiper-slide"><img src="{{baseurl}}/assets/images/ScreenControl.png" width="800px" /></div>
        <div class="swiper-slide"><img src="{{baseurl}}/assets/images/ScreenAdminProfil2.png" width="800px" /></div>
        <div class="swiper-slide"><img src="{{baseurl}}/assets/images/ScreenVolumes.png" width="800px" /></div>
        <div class="swiper-slide"><img src="{{baseurl}}/assets/images/ScreenTeacherWin10.png" width="800px" /></div>
    </div>
    <!-- If we need pagination -->
    <div class="swiper-pagination"></div>
 
    <!-- If we need navigation buttons -->
    <div class="swiper-button-prev"></div>
    <div class="swiper-button-next"></div>
 
</div>

## Aktuelles:

### **Fit für den Corona-Einsatz** (14.3.2020)

Die NextCloud ist bei uns seit über einem Jahr im Produktivbetrieb und hat sich als ausgesprochen stabil und produktiv erwiesen, so dass wir damit ganz entspannt in den Corona-Homeoffice-Modus gehen.

Aber eine Einschränkung gibt es: Das integrierte OnlyOffice in der Community-Edition ist nur für bis zu 20 Nutzer freigeschaltet, das ist leider zu knapp für eine vollständige Schulgemeinde im Coronavisus-Betrieb. Wir werden hier an Lösungen arbeiten.

### **Nextcloud- und OnlyOffice-Integration: Laufwerkszugriff auch von zu Hause (Beta)** (14.1.2019)

Ab sofort steht ein automatisches Setup für einen integrierten NextCloud-Container samt OnlyOffice-Installation bereit.

Alle Laufwerke sind damit von überall zugreifbar und Office-Dokumente sind sogar mit beliebigen Geräten direkt im Browser zu bearbeiten - und das sogar zeitgleich von mehreren Nutzern.

Beta-Testing: Wir setzen es bereits produktiv ein, ein paar Kleinigkeiten werden wir aber noch anpassen bevor wir es "stable" nennen.

Zu den [Info's für den Admin](/admins/NextCloud)

### **ftp-Server als optionaler Container** (9.12.2018)

Als Nebenprodukt bei der Entwicklung eines Nextcloud-Servers mit Zugriff auf die persönlichen Laufwerke ist ein ftp-Server im Container entstanden.

Einfach mit `git clone https://github.com/philleconnect/ftpServer` klonen und mit `docker-compose up -d` starten!

Eine genauere Anleitung, ggf. auch zum verschlüsselten Zugriff, wird bald folgen.

### **Optionaler Container RadiusServer** (22.6.2018)

PhilleConnect kann ab sofort zum authentifizierten Login ins WLan eingesetzt werden. Natürlich mit den vorhandenen Login-Daten.

Hier gibt's mehr Info's für [Admins](/admins/RadiusServer) oder [Anwender](/anwender/WLan)!

### **SummerStable 2018: v1.2.0 macht PhilleConnect fit für den Schuljahreswechsel** (4.6.2018)

Alle unsere ToDo's sind abgearbeitet, so gibt es eine sehr mächtige Funktion zum Jahrgangsübergang und viele weitere, auch weitgehende Verbesserungen und fixes.

Hier gibt's die Infos [wie man das Update einspielt](/admins/Betrieb) - ganz einfach und im laufenden Betrieb!

### **Fertig: PhilleConnect ist ab sofort als Stable Version v1.0.0 verfügbar!** (5.1.2018)

Und so sieht's aus: [Screenshots](/allgemein/Screenshots)!

Kurzanleitung zur [Installation](/admins/Installation) auf einem [Ubuntu](https://www.ubuntu.com/download/server){:target="_blank"} 18.04LTS-System:
* Auf der Kommandozeile `sudo apt install docker.io docker-compose git` ausführen
* dann mit `git clone http://github.com/philleconnect/ServerContainers/` PhilleConnect docker-Anweisungen holen
* mit `cd ServerContainers` in den passenden Ordner wechseln und bedarfsweise in der Datei `settings.env` eigene Passwörter vergeben
* und mit `sudo docker-compose up -d` die Server-Container bauen und starten (dauert nur beim ersten Start so lange).

Fertig ist die Serverlandschaft mit LDAP, Samba und PhilleConnect-Adminoberfläche, die unter `http://localhost:84/setup/` konfiguriert und mit einem Zugangspasswort versehen werden kann. Dort findet sich auch ein Link zum [Download des Client-Installers](https://github.com/philleconnect/ClientSetup-Windows/releases).

## **PHILLE**CONNECT: Schlank, modular, anpassbar, erweiterbar, verständlich, nützlich, fortschrittlich, systemübergreifend, frei. Hackable.
