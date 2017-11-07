---
layout: page
title: FAQ
permalink: /admins/Faq
tags: Admins
lang: de
---

# **FRAGEN**ANTWORTEN

### Muss ich als Admin Docker können?
Nein.

### Kann ich eigene Dienste mit dem integrierten LDAP authentifizieren?
Ja. Dazu muss in der `docker-compose.yml` der LDAP-Port freigegeben werden. Vielleicht findet sich in der [EntwicklerEcke](/entwickler) ja noch passende Information.

### Können ich und meine Kollegen oder auch die Schüler mit eigenen Geräten PhilleConnect nutzen?

Ja, der Samba-Server kann z.B. von jedem Windows-Gerät durch Eingabe von `\\<ip-oder-hostname-des-servers>\` erreicht werden.

Dinge wie die Monitorkontrolle zum Beispiel funktionieren natürlich nicht ohne installierten VNC-Dienst.

### Beinhaltet PhilleConnect eine Softwareverteilung?
Nein. Das hat erstmal nichts mit Schule zu tun, es gibt diverse Software da draussen für den Fall.

Eine (kostenlose) Lösung für die Software-Verteilung hat das Computermagazin C't zum Beispiel vor nicht all zu langer Zeit vorgestellt.

### Beinhaltet PhilleConnect eine Imaging-Lösung um fertige Installationen auf mehreren Rechnern zu verteilen.
Noch nicht.

Ich habe jedoch eine Imaging-Lösung auf der Grundlage eines Netzwerk-Debian-Systems und der Verwaltung des Image-Masters in VirtualBox in Betrieb. Zumindest den Boot-Server und eine Anleitung zur Image-Verwaltung möchte ich bei Zeiten als optionalen Container für PhilleConnect zur Verfügung stellen.

### Muss ich einen ipFire-Router in der Schule einsetzen?
Nein, jedoch funktioniert dann die Internetsperre nicht.

Wenn der Router, wie z.B. TimeForKids, eine Internetsperre mitbringt kann diese einfach weiter genutzt werden.

Auch wenn speziell TimeForKids an sich auf ipFire basiert ist diese Lösung nicht mehr frei genug um unsere Internetsperre dort einzusetzen. (Merke: Benutze nur freie Software! ;-)

### Beinhaltet PhilleConnect einen Festplattenschutz, der in vielen Schulen die PCs vor Veränderung und Manipulation schützt?

Leider nein.

Hier setze ich noch eine Kommerzielle Lösung ein.

Wenn Sie geeignete freie Software kennen, die wir vielleicht integrieren können, lassen Sie es uns wissen!
