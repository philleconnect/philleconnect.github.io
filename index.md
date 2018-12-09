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

### **ftp-Server als optionaler Container** (9.12.2018)

Als Nebenprodukt bei der Entwicklung eines Nextcloud-Servers mit Zugriff auf die persönlichen Laufwerke ist ein ftp-Server im Container entstanden.

Einfach mit `git clone https://github.com/philleconnect/ftpServer` klonen und mit `docker-compose up -d` starten!

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
