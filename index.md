---
layout: default
permalink: /index.html
---

# **PHILLE**CONNECT

## Schul-IT der nächsten Generation Schul-IT: PhilleConnect ist eine moderne, modulare und anpassbare OpenSource Schulnetzwerk-Lösung

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

### **Fertig: PhilleConnect ist ab sofort als Stable Version v1.0.0 verfügbar!** (5.1.2018)

Und so sieht's aus: [Screenshots](/allgemein/Screenshots)!

Kurzanleitung zur [Installation](/admin/Installation) auf einem [Ubuntu](https://www.ubuntu.com/download/server)-System:
* Auf der Kommandozeile `sudo apt-get install docker docker-compose git` ausführen
* dann mit `git clone http://github.com/philleconnect/ServerContainers/` PhilleConnect docker-Anweisungen holen
* mit `cd ServerContainers` in den passenden Ordner wechseln und bedarfsweise in der Datei `settings.env` eigene Passwörter vergeben
* und mit `sudo docker-compose up -d` die Server-Container starten

Fertig ist die Serverlandschaft mit LDAP, Samba und PhilleConnect-Adminoberfläche, die unter `http://localhost:84/setup/` konfiguriert und mit einem Zugangspasswort versehen werden kann. Dort findet sich auch ein Link zum [Download des Client-Installers](https://github.com/philleconnect/ClientSetup-Windows/releases/download/1.0.2/PhilleConnectSetup.exe).

## **PHILLE**CONNECT: Schlank, modular, anpassbar, erweiterbar, verständlich, nützlich, fortschrittlich, Systemübergreifend, frei. Hackable.
