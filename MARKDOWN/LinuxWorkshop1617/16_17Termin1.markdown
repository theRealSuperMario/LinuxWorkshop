# 16 17Termin1
Created Dienstag 25 Oktober 2016


Wlan Einrichten
---------------
Kit wlan: im akk: Anonymous Identity: " [anonymous@kit.edu](mailto:anonymous@kit.edu)"
Ca certificate: /etc/ssl/certs/Deutsch_Telekom_Root_CA_2.pem
Inner authentication: Dropdown "PAP"
Username/Passwort: Kit Account

![](./16_17Termin1/pasted_image.png)	
![](./16_17Termin1/pasted_image001.png)

mehr infos dazu auf der seite des SSC

Ubuntu Unity
------------
<http://wiki.ubuntuusers.de/Unity>

### Tastatursprache Umstellen

### die Launcher Leiste:

* Dash
	* wie das Startmenü in Windows.
	* außerdem auch kürzlich verwendete Dokumente, Internetsuche [wikipedia, ...] → Barack Obama
* Dateien / Files im Englischen [Nautilus] <https://wiki.ubuntuusers.de/Nautilus>
	* genau wie normaler Explorer, mit möglichen Plugins
	* STRG+H für versteckte Dateien
	* STRG+T neuer Tab
	* F9
	* Mit der Tastenkombination  Strg +  L lässt sich die Adressleiste einschalten. → manuelle Adresse eingeben
	* Dateien mit andere Anwendung öffnen
	* Dateien erstellen
	* Auf Windows Platte zugreifen
	* auf USB Stick zugreifen
	* Screenshot machen → man findet ihn mit Bildern. Croppen mit Shotwell Viewer
* Firefox
* LibreOffice Programme
	* <https://de.libreoffice.org/discover/templates-and-extensions/users/>
	* libre office maths
* mehrere Arbeitsflächen
	* System Settings → 
	* Tastenkürzel übersicht SUPER lang gedrückt halten. [super = Windowstaste]
* Überleitung Dateiinstallation: Plugin für Files

![](./16_17Termin1/pasted_image002.png)


Warum Linux
-----------


* Linux ist ein sehr zuverlässiges System
* Es kommen immer wieder Leute und erzählen, dass ihr Windows über Nacht abgeschmiert ist und sie froh waren, dass sie Ihre Daten mit einem Linux-Live-Stick retten konnten
* Linux empfiehlt sich auch für ein Dualboot Setup (Windows / Linux) 
	* selbst wenn Linux nur im Notfall verwendet wird
		* Ausfallsicher, weniger Hassel
		* Linux brauch nicht viel Platz


Dateistruktur
-------------


Die wichtigesten Ordner sind hier kurz vorgestellt. Für diejenigen, die Linux nur zum Surfen und Hausarbeiten erstellen verwenden, wird dieser Abschnitt eher unwichtig sein. 

##### "/" - (Root)
Der sogenannte *root-*Ordner ("/////") in Linux ist das oberste Dateiverzeichnis im System, von dem aus alle anderen Verzeichnisse erreichbar sind. 


##### "/home"
Im *home *Verzeichnis sind die Ordner der jeweiligen Benutzer enthalten. Im Homeverzeichnis eines Benutzers befinden sich die Einstellungen zu Programmen und dem System, sowie seine privtaten Dokumente. Programmeinstellungen sind i.d.R. in versteckten Dateien/Ordnern hinterlegt (In Linnux werden Dateien/Ordner verstekckt, indem im Dateinamen ein Punkt "." vorangestellt wird).


##### "/etc"
*etc *steht, e nach Quelle, für "editable text configuration" oder "et cetera".  Hier sind Systemeinstellungen wie Netzwerkverbindungen und Einstellungen der graphischen Benutzeroberfläche in Textform gespeichert. Im Workshop haben wir den Ordner"/*etc/ssl/certs*/" gebraucht um das richtige Zertifikat für die Wlan-Verbindung im Akk zu wählen.

##### "/dev"
enthält Dateien die notwendig sind um Geräte (engl.: **dev**ices) und Hardware anzusprechen .

##### "/media"
Hier werden, unter dem jeweiligen Benutzernamen, mediendatenträger wie USB Sticks und externe Festplatten eingebunden.

##### "/mnt"
Hier können Festplatten/Partitionen tempörar oder auch dauerhaft eingebunden werden. Automatisch werden diese jedoch unter "[/media/<benutzername](file:///C:/media/%3Cbenutzername)>" eingebunden.

##### "/tmp"
Dieses Verzeichnis ist für temporäre Datein gedacht, die nach Verwendung verschoben oder gelöscht werden.

##### "/bin"
Enthält grundlegende **bin**äre Programme, die das System braucht um ordnungsgemäß funktionieren zu können.

##### "/usr"
Hier liegen die meisten installierten Programme die für alle Benutzer zugänglich sind.

##### "/root"
Dieses Verzeichnis dient dem *root-user *als Homeverzeichnis. Es befindet sich nicht im *home-*Verzeichnis mit den anderen, da es beim Systemstart auf jeden Fall sofort zugänglich sein muss und *home *oft auf einer anderen Festplatte oder sogar irgendwo im Netzwerk zu finden ist und erst eingebunden werden muss. Ist von dem *root-*Verzeichnis die Rede, ist meistens nicht diese Verzeichnis gemeint, sondern "/".

Weitere Infromationen siehe <https://wiki.ubuntuusers.de/Verzeichnisstruktur/>.


### Installieren von Programmen in Ubuntu
3 Möglichkeiten:

1. sudo apt-get install [aus Packetquellen, fremd oder official] → beispiel gnome-sushi
2. download einer installationsdatei aus dem web	z.B. google-chrome, skype
3. softwareshop. gleiche wie sudo apt-get install, nur grafisch	ubuntu restricted Extras
	a. der erfahrene Linuxnutzer verwendet meist sudo apt-get install, da es tausendmal schneller geht.
4. herunterladen eines zip / ordners aus dem web OHNE INSTALLATION. Meist muss dann in den bin Ordner gewechselt werden und das start Skript in einem Terminal ausgeführt werden
	a. → Workshop 3	[Bsp.: Matlab, Eagle,...]


Was nicht geht sind .exe datein, die sind Windows only. Man sollte nach Ubuntu / Debian installationsdateien suchen. [.deb, ]

"ubuntu restricted extras" aus dem software center. wichtig für alle die was mit medien machen, zb
treiber/bibliotheken für audio/video/... dateien. Am besten als erstes runterladen


* Idee von dependencies: Viele Programme bauen auf anderen Programmen auf. Damit der Nutzer nicht selbst schauen muss, welche Abhängigkeiten gebraucht werden, macht apt-get und das softwarecenter das von selbst und sagt einem, dass man die progrmme auch mit installieren muss.
* bei Downloads aus dem Internet oft nicht so, da apt-get nicht aufgerufen wird.
	* → selbst auf der Software seite schauen, was der Entwickler sagt, welche software mitinstalliert werden muss
	* googlen
	* <https://wiki.ubuntuusers.de/Startseite> → bestes Hilfeforum für fast alles. also immer erst dort schauen.


### System Update durchführen

	#aktualisiert die packetquellen
	sudo apt-get update 
	
	#update durchführen
	sudo apt-get upgrade


### Deinstallieren von Software


1. via Terminal

	sudo apt-get remove softwarename
	
	## nicht benötigte software automatisch entfernen
	sudo apt-get autoremove
	
	## software entfernen UND zugehörige Programmdatein aus home lösen
	sudo apt-get purge softwarename

![](./16_17Termin1/pasted_image004.png)


<https://wiki.ubuntuusers.de/apt/apt-get?redirect=no>

2. grafisch über das Softwarecenter




Ubuntu Versionen
----------------
<https://wiki.ubuntuusers.de/Steckbriefe_der_Ubuntuversionen/>

Ubuntu 14.04 (LTS version)
Trusty Tahr
![](./16_17Termin1/pasted_image015.png)
Ubuntu 14.10
Utopic Unicorn
![](./16_17Termin1/pasted_image016.png)

Ubuntu 15.04
Vivid Vervet 
![](./16_17Termin1/pasted_image017.png)

Ubuntu 15.10
Wily Wirewolf
![](./16_17Termin1/pasted_image018.png)
Ubuntu 16.04 (LTS Version)
Xenial Xerus
![](./16_17Termin1/pasted_image019.png)

Ubuntu 16.10
Yakkety Yak
![](./16_17Termin1/pasted_image020.png)



Releasestrategie: 
Alle 2 Jahre neue LTS version (12.04, 14.04, 16.04). LTS = Long-Term-Support
Nächster Release im April 2017 ( 17.04 ) Welchers Tier beginint mit Z?
![](./16_17Termin1/pasted_image021.png)

![](./16_17Termin1/pasted_image022.png)


Weitere Linux-Distributionen
----------------------------




Aktuelles zu Open-Source,Linux und Ubuntu
-----------------------------------------

![](./16_17Termin1/pasted_image010.png)
<http://www.ros.org/install/>

Wer benutzt ROS?
<https://developer.dji.com/onboard-sdk/documentation/introduction/architecture-guide.html>

![](./16_17Termin1/pasted_image012.png)

![](./16_17Termin1/pasted_image013.png)





<https://insights.ubuntu.com/2016/09/07/welcoming-the-parrot-s-l-a-m-dunk-the-new-drone-development-kit/>
![](./16_17Termin1/pasted_image009.png)
"
Parrot collaborates with Canonical to launch the Parrot S.L.A.M.dunk, a new development kit for the creation of autonomous and obstacle avoidance drones and robots. 
Powered by Ubuntu and ROS (Robot Operating System), it gives developers a familiar environment to prototype solutions such as 
autonomous driving, 3D mapping, or simply using the on board stereo camera and sensors for data gathering.
"


<https://wiki.ubuntuusers.de/Steam/>
![](./16_17Termin1/pasted_image014.png)



2016-11-16
![](./16_17Termin1/pasted_image008.png)


Bsp: zim



### Gnome

* Tastatursprache umstellen 
	* Systemsettings → Keyboard → [unten links im eck] Layouts → Input Sources → + → German


### gnome plugins
gnome icon overlay





