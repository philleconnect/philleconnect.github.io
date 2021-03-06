---
layout: page
title: FAQ
permalink: /admins/Faq
tags: Admins
lang: de
---

# **FRAGEN**ANTWORTEN

(Diese Seite wird ergänzt wenn uns relevante Fragen zugetragen werden)

Sie können **mit `Strg` + `F` diese Seite durchsuchen**!

### Muss ich als Admin **Docker beherrschen**?
Nein.

### Kann ich **eigene Dienste** mit dem integrierten **LDAP** authentifizieren?
Ja. Dazu muss in der `docker-compose.yml` der LDAP-Port freigegeben werden. Vielleicht finden sich in der [EntwicklerEcke](/Entwickler) ja noch passende erweiterte Information.

### Können meine Kollegen und ich, oder auch die SchülerInnen, mit **eigenen Geräten** PhilleConnect nutzen?
Ja, der Samba-Server kann z.B. von jedem Windows-Gerät durch Eingabe von `\\<ip-oder-hostname-des-servers>\` im Explorer erreicht werden, von Linux-Geräten oft durch Eingabe von z.B. `smb://<ip-oder-hostname-des-servers>/`.

Dinge wie die Monitorkontrolle funktionieren natürlich nicht ohne installierten VNC-Dienst.

### Beinhaltet PhilleConnect eine **Softwareverteilung**?
Nein. Gemäß dem [KISS-Prinzip](/Allgemein) glauben wir an "One Job - one Tool".

Das hat nichts mit Schule zu tun, es ist für uns nicht erkennbar warum das fester Bestandteil einer Schulnetzwerklösung sein sollte, es gibt diverse Software da draussen für den Fall.

Eine (kostenlose) Lösung für die Software-Verteilung hat das Computermagazin C't zum Beispiel in Heft 17/2017, S.162ff vorgestellt.

Sollte jemand eine freie Lösung zum Beispiel als Docker-Container [entwickeln](/Entwickler) nehmen wir diese gerne als optionalen Container mit auf.

### Beinhaltet PhilleConnect eine **Imaging-Lösung** um fertige Installationen auf mehreren Rechnern zu verteilen.
Nein. Siehe auch oben.

Wir empfehlen hierfür die Open-Source-Lösung [FOG-Project](https://fogproject.org), die sehr Leistungsfähig uns flexibel ist, einschließlich einiger Aufgaben nach dem Imagen. Das [ALP Dillingen](https://alp.dillingen.de/) hat dazu eine [gute Anleitung](http://schulnetz.alp.dillingen.de/materialien/Fog.pdf) bereit gestellt.

Möglicherweise werden wir hierfür in Zukunft ein SnapIn zu Verfügung stellen, welches nach dem Imagen automatisch den PhilleConnect-Client installiert.

### Muss ich einen **ipFire-Router** in der Schule einsetzen?
Nein, jedoch funktioniert dann die Internetsperre nicht.

Wenn der Router, wie z.B. TimeForKids, eine Internetsperre mitbringt kann diese einfach weiter genutzt werden.

Auch wenn speziell TimeForKids auf ipFire basiert, ist diese Lösung nicht mehr frei genug um unsere Internetsperre dort einzusetzen. (Merke: Benutze nur freie Software! ;-) Wer doch eine Möglichkeit findet - gerne berichten!

### Beinhaltet PhilleConnect einen **Festplattenschutz**, wie er in vielen Schulen die PCs vor Veränderung und Manipulation schützt?

Nein.

Microsoft Windows hat dafür die Lösung [Disk Protection](https://docs.microsoft.com/en-us/windows-server/remote/multipoint-services/enable-or-disable-disk-protection) vorgesehen, für manche mag das eine Lösung sein, jedoch setzt dies auf den MultiPoint-Services auf, was nicht für jedermann brauchbar sein dürfte.

Eine alternative ist die Arbeit mit [Restore Points](https://msdn.microsoft.com/en-us/library/aa378910(VS.85).aspx) was wir uns in absehbarer Zeit mal genauer anschauen wollen.

(Wir selbst kennen es auch erst seit kurzem und müssen es noch ausprobieren, ob es unsere bisherige kommerzielle Lösung ersetzen kann)

Für Linux bietet es sich da die Systempartition mit der `/ets/fstab` als read-only zu mounten.

### Gibt es einen **Klausur- oder Test-Modus** um Klassenarbeiten und Klausuren zu schreiben?

Leider noch nicht.

Es fehlt noch eine überzeugende Idee, wie man einen im Netz hängenden Rechner, an dem der Benutzer eigenen Code ausführen kann, (was in Informatikklausuren unumgänglich ist) einen Oberstufen-festen Klausurmodus implementieren kann.

Wir sind gerne offen für Ideen!

### Wie kann ich dann **Klausuren schreiben**?

Ich mache es so: Ich verteile die Klausur per Raumtausch-Laufwerk, dann lasse ich das Netzwerkkabel abziehen. Wer fertig ist steckt das Kabel wieder ein und legt seine Ergebnisse in einen Ordner mit seinem Namen im Tauschlaufwerk ab.

Zugegeben, recht brute-force. Aber überzeugend sicher.

Neue Ideen sind herzlich willkommen!

### Was ist mit der ebenfalls freien Lösung **[LinuxMuster.net](https://linuxmuster.net){:target="_blank"}** ? ###

Uns ist es zu umfangreich, zu unverständlich und nicht modular genug. Es fehlt uns die Flexibilität und der problemlose Übergang der bestehenden Lösung. Fertige Systemimages bleiben ein Stück weit Magie, wir finden Infrastructure-as-Code ist schlicht besser.

Wir hoffen durch unsere Lösung mehr Ideen beizusteuern, vielleicht können wir ja dann von einander lernen, möglicherweise wechselseitig auch Dinge übernehmen.

Wer neu hier ist: Wir empfehlen auf jeden Fall auch dort mal vorbei zu schauen, auf manche mag die MusterLösung "mit allem, was man braucht. Und mehr." sogar besser passen als PhilleConnect, was [NUR das bietet was man braucht](/Allgemein){:target="_blank"}.

Wir sind aber Stolz auf das was uns auszeichnet: schlank, modular, anpasspar, erweiterbar, verständlich. Hackable.

### Was ist mit der hessischen Lösung **[LANiS](https://lanis-system.de){:target="_blank"}**?

Das Schulnetzwerk von LANiS war an vielen Stellen unser Vorbild bei der Entwicklung von PhilleConnect, jeder der umsteigt wird dies deutlich erkennen.

Jedoch haben uns so viele Dinge an LANiS gestört, dass wir uns entschieden haben eine eigene Lösung zu entwickeln: Geboren in den 90ern basiert LANiS (aus unserer Sicht unnötigerweise) auf einem Windows-Domänen-Netzwerk, was viel Ärger mit sich bringt (Kenner kennen z.B. DNS-Probleme oder langsame Bootzeiten).

Gleichzeitig ist LANiS nicht Quelloffen, viele Ideen konnten wir nicht umsetzen, einige Entwicklungen waren aus unserer Sicht eher zum Schaden als zum Nutzen. Die Zukunftsfähigkeit wird nicht nur von uns bezweifelt, die allgemeine Softwarequalität und die Unübersichtlichkeit gaben schließlich den Ausschlag unsere eigene Lösung zu entwickeln.

Siehe auch: [Philosophie](/Allgemein) oder [Umstieg](/admins/Umstieg)

### Ich habe etwas bei der Konfiguration falsch gemacht/nur mal rum gespielt, wie kann ich die **Container samt der Installation wieder löschen** und von vorne anfangen?

Wenn die `./dev/cleanup.sh` ausführen wird jede Konfiguration samt Datenbanken, LDAP etc. gelöscht.

Führen Sie dies niemals für ein bereits laufendes System aus, da alle Daten unwiederbringlich verloren gehen!
