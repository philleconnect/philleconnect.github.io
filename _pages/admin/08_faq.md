---
layout: page
title: FAQ
permalink: /admin/Faq
tags: Admins
lang: de
---

# **FRAGEN**ANTWORTEN

### Muss ich als Admin Docker können?
Nein.

### Kann ich eigene Dienste mit dem integrierten LDAP authentifizieren?
Ja. Dazu muss in der `docker-compose.yml` der LDAP-Port freigegeben werden. Vielleicht finden sich in der [EntwicklerEcke](/entwickler) ja noch passende erweiterte Information.

### Können ich und meine Kollegen, oder auch die Schüler, mit eigenen Geräten PhilleConnect nutzen?

Ja, der Samba-Server kann z.B. von jedem Windows-Gerät durch Eingabe von `\\<ip-oder-hostname-des-servers>\` im Explorer erreicht werden, von Linux-Geräten oft durch Eingabe von z.B. `smb://<ip-oder-hostname-des-servers>/`.

Dinge wie die Monitorkontrolle funktionieren natürlich nicht ohne installierten VNC-Dienst.

### Beinhaltet PhilleConnect eine Softwareverteilung?
Nein.

One Job - one Tool.

Das hat nichts mit Schule zu tun, es ist für uns nicht Erkennbar warum das fester Bestandteil einer Schulnetzwerklösung sein sollte, es gibt diverse Software da draussen für den Fall.

Eine (kostenlose) Lösung für die Software-Verteilung hat das Computermagazin C't zum Beispiel in Heft 17/2017, S.162ff vorgestellt.

Sollte jemand eine freie Lösung zum Beispiel als Docker-Container [entwickeln](/entwickler) nehmen wir diese gerne als optionalen Container mit auf.

### Beinhaltet PhilleConnect eine Imaging-Lösung um fertige Installationen auf mehreren Rechnern zu verteilen.
Nein.

Siehe auch oben.

Ich habe jedoch eine Imaging-Lösung auf der Grundlage eines Netzwerk-Debian-Systems und der Verwaltung des Image-Masters in VirtualBox in Betrieb. Zumindest den Boot-Server und eine Anleitung zur Image-Verwaltung möchte ich bei Zeiten als optionalen Container für PhilleConnect zur Verfügung stellen.

### Muss ich einen ipFire-Router in der Schule einsetzen?
Nein, jedoch funktioniert dann die Internetsperre nicht.

Wenn der Router, wie z.B. TimeForKids, eine Internetsperre mitbringt kann diese einfach weiter genutzt werden.

Auch wenn speziell TimeForKids an sich auf ipFire basiert ist diese Lösung nicht mehr frei genug um unsere Internetsperre dort einzusetzen. (Merke: Benutze nur freie Software! ;-) Wer doch eine Möglichkeit findet - gerne berichten!

### Beinhaltet PhilleConnect einen Festplattenschutz, wie er in vielen Schulen die PCs vor Veränderung und Manipulation schützt?

Leider nein.

Hier setzen wir noch eine kommerzielle Lösung ein.

Wenn Sie geeignete freie Software kennen, die wir integrieren könnten, lassen Sie es uns wissen!

### Gibt es einen Klausur-Modus um Klassenarbeiten und Klausuren zu schreiben?

Leider noch nicht.

Es fehlt noch eine überzeugende Idee, wie man einen im Netz hängenden Rechner, an denen der Benutzer eigenen Code ausführen kann (was in Informatikklausuren unumgänglich ist), einen Oberstufen-festen Klausurmodus implementieren kann.

Wir sind gerne offen für Ideen!

### Wie kann ich dann Klausuren schreiben?

Ich mache es so: Ich verteile die Klausur per Raumtausch-Laufwerk, dann lasse ich das Netzwerkkabel abziehen. Wer fertig ist steckt das Kabel wieder ein und legt seine Ergebnisse in einen Ordner mit seinem Namen ins Tauschlaufwerk.

Zugegeben, recht brute-force. Aber überzeugend sicher.

Neue Ideen sind herzlich willkommen!

### Was ist mit der ebenfalls freien Lösung [LinuxMuster.net](https://linuxmuster.net) ? ###

Sorry, liebe LinuxMuster, aber uns ist es zu umfangreich, zu unverständlich und nicht modular genug. Es fehlt uns die Flexibilität und der problemlose Übergang der bestehenden Lösung. Fertige Systemimages bleiben ein Stück weit Magie.

Wir hoffen durch unsere Lösung mehr Ideen bei zu steuern, vielleicht können wir ja dann von einander lernen, möglicherweise wechselseitig auch Dinge übernehmen.

Wer neu hier ist: Wir empfehlen auf jeden Fall auch dort mal vorbei zu schauen, auf manche mag die MusterLösung "mit allem, was man braucht. Und mehr." sogar besser passen als PhilleConnect, was [NUR das bietet was man braucht](/Allgemein){:target="_blank"}.

Wir sind aber Stolz auf das was uns auszeichnet: schlank, modular, anpasspar, erweiterbar, verständlich. Hackable.
