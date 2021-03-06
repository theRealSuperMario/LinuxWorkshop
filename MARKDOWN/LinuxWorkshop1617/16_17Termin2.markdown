# 16 17Termin2
Created Dienstag 25 Oktober 2016


Sandro
------

#### PDFJAM oder PDFTKz
Tools um pdfs in der kommandozeile manipulieren

beispiel: Vorlesungsfolien auf 1 Seite mit Platz für Notizen komprimieren
	pdfjam --nup 1x3 --no-landscape --frame false --offset '-4cm 0cm' --trim '0.5cm 0.5cm 0.8cm 0.8cm' bar.pdf


### KDE 5
Top Features: 

* Activities
	* Nicht nur mehrere Desktops, sondern nach "Aktivität" getrennte Desktop sets
* Widgets
	* KDE connnect - nahtlose Integration des Smartphones (Android)
	* Sticky notes
	* Event Calendar
* Shortcuts für ALLES
	* fenster auf den zweiten monitor verschieben, kacheln, ....
	* Maus-gesten
* Fast beliebig personalisierbar, theme manager, etc...
* K runner (alt + F2 oder alt + leertaste)
* Dolphin: Terminal und Split-view
* eigene Kontrollleisten




### Alternativprogramme

Sehr gute übersicht zu alternativprogrammen für kreative:
<http://www.makeuseof.com/tag/free-alternatives-photoshop-illustrator-lightroom/>
| Windowsprogramm         | Open-Source-Alternative                                                                               | Bemerkung                                                                                                                                                                                                                                                                                      |
|:------------------------|:------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| OneNote                 | Zim sehr empfehlenswert aus eigener Erfahrung <br> ansonsten einfach nach "Desktop-Wiki" googlen      | Für Zim werden ein paar andere Plugins benötigt, siehe im Abschnitt zim                                                                                                                                                                                                                        |
| Lightroom, Bridge       | Digikam bzw Digikam5 (Projekt der KDE Community), platformunabhängig <br> Darktable (Mac, Linux), Raw | offizielle Projektwebseite: <https://www.digikam.org/> <br> Leider gibt es bisher einen BUG für die Installation vom Sourcecode, weshalb dieser Artikel sehr hilfreich für die Installation ist: <br> <http://ubuntuhandbook.org/index.php/2016/07/install-digikam-5-0-kubuntu-16-04-via-ppa/> |
| Illustrator             | Inkscape                                                                                              |                                                                                                                                                                                                                                                                                                |
| Photoshop               | Gimp                                                                                                  |                                                                                                                                                                                                                                                                                                |
| youtube 2 mp3 converter | clipgrab                                                                                              | eine menge abhängigkeiten.... siehe ubuntuusers <br> <https://wiki.ubuntuusers.de/Clipgrab>                                                                                                                                                                                                    |
| Itunes                  | Amarok (KDE spezifisch)                                                                               |                                                                                                                                                                                                                                                                                                |
| Bücherregal Software    | Calibre                                                                                               |                                                                                                                                                                                                                                                                                                |


Alternative zu Matlab: Gnu Octave oder halt gleich Python mit Scipy Stack
<https://www.gnu.org/software/octave/>
![](./16_17Termin2/pasted_image008.png)
	sudo apt-get install octave* ##installiert alle programme




Matlab geht aber auch problemlos auf Linux. Beachte die Installationshinweise

Es gibt eine Menge guter Alternativen, man sollte sich am besten einfach umsehen.


#### Installation von Matlab

installation mit sudo starten
create symbolic links: ja
Nutzername auf sandro ändern
<http://askubuntu.com/questions/758892/matlab-not-work-on-ubuntu-16-04>

Probleme bei Ubuntu 16.04 und Matlab
![](./16_17Termin2/pasted_image009.png)

Keyboard -> Shortcuts-> Windows Default Set
Matlab -> Editor/Debugger -> Code Folding -> enable all


#### Hinweise zu Zim

**Zim ist** ein sogennanntes Desktop Wiki. Davon gibt es viele, Zim ist aber aufgrund der Schlichtheit sehr beliebt. Zim funktioniert ausschließlich mit .txt Dateien und Ordnern und eigent sich daher ideal für Dropbox und sharing.
![](./16_17Termin2/pasted_image.png)


Die Version befindet sich noch in der Version 0.xx. Es werden deshalb noch einge nützliche Features kommen und nicht alles funktioniert ohen Probleme.
Häufigstes Problem: Die Seite lässt sich nicht bearbeiten / reagiert nicht. Mit dem Mausrad scrollen beseitigt das Problem. Wenn die Seite zu klein ist, sollte man einfach ganz oft 
Eingabe drücken und dann wird es irgendwann funktionieren.


**Installation** empfiehlt sich aufgrund der sofortigen Verfügbarkeit direkt aus dem PPA des Entwicklers
	sudo apt-add-repository ppa:jaap.karssenberg/zim
	sudo apt-get update
	
	sudo apt-get install zim
	
	## this is required for all the nice plugins
	sudo apt-get install libzeitgeist-dev scrot python-gtksourceview2 graphviz python-blockdiag


### Warum open-source super ist

Wenn man zim mit einem "dark-theme" benutzt, hat man das Problem, dass die Gleichungen kaum sichtbar sind.
![](./16_17Termin2/equation.png)

Zum Glück ist Zim open-source und man kann den Quellcode einsehen. Aus der Hilfeseite kann man sehen, dass die Umwandlung in ein png
durch das dvipng command-line tool passiert. Findet man also die Zeile code, die den entsprechenden Aufruf tätigt, kann man sich vllt behelfen.

[/usr/lib/python2.7/dist-packages/zim/plugins/equationeditor.py](file:///C:/usr/lib/python2.7/dist-packages/zim/plugins/equationeditor.py)
![](./16_17Termin2/pasted_image001.png)

Wenn man diese Zeile ändert, erhält man was man möchte: weißen hintergrund. Hier wurde noch etwas mehr gemacht. Das Programm muss allerdings zuerst neu gestartet werden.

![](./16_17Termin2/equation.png)





#### digikam5

**digikam5** Cross-Platform Konkurrenz zur Adobe Produktkette Lightroom - Bridge - zum Teil auch Photoshop zu sein. Natürlich gibt es noch mehr alternativen, digiKam ist nur eine.
<https://docs.kde.org/trunk5/en/extragear-graphics/digikam/digikam.pdf>

**Installation**
Bei der Installation sollte dieser Artikel beachtet werden.
<http://ubuntuhandbook.org/index.php/2016/07/install-digikam-5-0-kubuntu-16-04-via-ppa/>


### Falls es mal doch kein Alternativprogramm geben sollte
Dann gibt es nur noch zwei Möglichkeiten, ein Windowsprogramm unter Linux zu nutzen


#### Wine
Read first: <https://wiki.ubuntuusers.de/Wine>

WINE (Kompatibilität erzeugen) - Wine is not an emulator [WINE]

**Installation via Repository: (Achtung, dauert)**
	sudo add-apt-repository ppa:ubuntu-wine/ppa
	sudo apt-get update
	sudo apt-get install wine1.6


Prüfen, ob die Software die man verwenden möchte gut mit Wine funktioniert über <https://appdb.winehq.org/>
⇒ 4 Stufen: Garbage - Silver - Gold - Platinum
![](../LinuxWorkshop/Termin_3/pasted_image.png)

**BSP LT SPICE**


1. Download von <http://www.linear.com/designtools/software/#LTspice>
2. Doppelklick auf Heruntergeladene Datei
	a. ![](./16_17Termin2/pasted_image003.png)
3. Windows Installer erscheint und fragt nach Installation Directory. **!Wichtig** Das ist kein Linux Pfad. Also am besten einfach so lassen

![](./16_17Termin2/pasted_image004.png)


4. Das Programm kann nun wie gewohnt durch das Dash (oder sonst wie) gestartet werden

![](./16_17Termin2/pasted_image005.png)


![](./16_17Termin2/pasted_image006.png)




#### Virtual Box ( ein KOMPLETTES Windows System erzeugen )


* **Umbedingt zuerst die Host plugins installieren**
	* sonst ist keine bidirektionale ( == gemeinsame) Zwischenablage oder gemeinsame Ordner verwendbar.
* Für Office produkte sehr empfehlenswert (Powerpoint aus eigener Erfahrung)
* Funktioniert sehr gut. Bei leistungsschwachen Rechner sollte man nicht allzu viel nebenher am PC machen.
* **Definitiv keine Schande**
	* In manchen Unternehmen wird aus IT sicherheitsgründen eine Linux-VM auf einem Windows Rechner genutzt und ausschließlich in der Linux-VM entwickelt.
* Bei Fragen ⇒ Email an uns


![](./16_17Termin2/pasted_image002.png)


Warum command-line installation so praktisch ist
------------------------------------------------

Wenn man sich einfach aufschreibt, was man so über die Zeit installiert und was funktioniert, dann hat man ein Skript, dass man einfach
ausführt wenn man den PC neu aufsetzt.

* persönliches Beispiel: Mitten in meiner Bachelorarbeit kam ich nicht mehr in Ubuntu rein. DA ich meine persönlichen Daten auf eine Extra Partition ausgelagert hatte schonmal kein Datenverlust (Y)
* Abends dann einfach Ubuntu neu installiert (halbe STD). Anschließend das Skript durchlaufen gelassen (nochmal halbe STD) und dann noch ein paar andere Einstellungen vorgenommen.
* Nach 2 h war alles wieder wie vorher und funktionsfähig
* Das automatisierungspotential ist noch lange nicht ausgeschöpft. Allerdings ist nicht alles so einfach wie sich die "apt-get" Befehle aufzuschreiben


**Mit Linux hat man zumindest die Möglichkeit, einfach Dinge zu automatisieren, wenn man will und bereit sich ein bischen in bash-skripte einzuarbeiten.**


![](./16_17Termin2/pasted_image007.png)


Max
---

#### Startmedien
Möchte man sich selbst einen USB Livestick erstellen kann das mit verschiedenen Programmen sowohl unter Windows als auch unter Linux erstellt werden. Mit einem USB Livestick wie er im Workshop genutzt wurde kann Linux getestet werden ohne es auf dem PC zu installieren. Die Programme sind i.d.R. selbst erklärend. Zunächst muss ein geeigneter USB ausgewählt werden, der min. 4GB groß ist und auf dem keine 

##### wichtigen Dateien mehr gespeichert sind!!!

denn diese sind nach der Erstellung unwiederbringlich gelöscht. Danach wird ausgewählt welche Variante von Linux auf dem USB Stick installiert werden soll. Das dafür benötigte *Image *kann entweder direkt über das Programm heruntergeladen werden oder wird über die Website der jeweiligen Entwickler heruntergeladen. Bei den meisten Programmen kann noch die Größe des persistenen Speichers gewählt werden. Dieser sorgt dafür, dass Änderungen die auf dem USB Stick gemacht werden, auch dauerhaft sind. Ohne diesen Speicher setzt sich Linux nach jedem Neustart auf den Ursprungszustand zurück. Gemachte Einstellungen und erstellte Dateien gehen dabei verloren. Das ist eine Besonderheit von USB Livesticks, die bei einer richtigen Installation von Linux auf dem Rechner nicht mehr auftritt.

Aus unsere Erfahrung haben sich folgende Programme zu Erstellung solche USB Livesticks bewährt.

Unter Windows:

#### Lili USB Creator
![](./16_17Termin2/lili_usb_creator.PNG)

#### UNetbootin
![](./16_17Termin2/UNetbootin_usb_creator.PNG)

Unter Linux:
------------
Die meisten Linuxinstallationen bringen einen Startmedienersteller mit sich. Ansonsten ist es mit *Mulisystem *möglich sogar mehrer Linuxvarianten auf einem USB Stick gleichzeitig zu erstellen. *Multisystem *wurde auch für die verwendung der Sticks für den Workshop verwendet. Die Installation sowohl des Programms als auch der Sticks ist allerdings etwas aufwendiger als der der anderen. Nähere Infos siehe <https://wiki.ubuntuusers.de/MultiSystem/>

![](./16_17Termin2/multisystem2.png)

#### Terminal

Terminal
========

![](./16_17Termin2/Terminal)

Übersicht Terminal:
-------------------
Öffnet man ein Terminal sieht man zunächst die sogenannte *Prompt. *Im obigen Beispiel lautet diese *max@max-mint18 ~ $. *Diese sieht bei jedem Benutzer anders aus. Allgemein zeigt sie i.d.R. 
<akutell eingeloggter Benutzer>@<Name des Rechners> <aktuelles Arbeitsverzeichnis>  $
im obigen Beispiel ist also der Benutzer *max *eingeloggt auf dem Rechner *max-mint18. *
Das Arbeitsverzeichnis ist hier das Homeverzeichnis des Benutzers, abgekürzt mit dem *~ *Symbol.

Häufig verwendete Befehle
-------------------------

##### cd - Verzeichnis wechseln
Möchte man das aktuelle Arbeitsverzeichnis ändern, kann man das mit dem *cd *Befehl gefolgt vom gewünschten Pfad. Angenommen wir befinden uns im Homeverzeichnis und wollen in den darin befindlichen Ordner *Documents * wechseln, können wir entweder:

* den vollen absoluten Pfad /*home/max/Documents *
* den relativen Pfad *~/Documents*
* den Ordnernamen *Documents*

eingeben. Alle drei Möglichkeiten führen zum selben Ergebnis. Zu beachten ist hierbei, dass wir die ersten beiden Varianten aus jedem Verzeichnis heraus verwenden können, da "*~" * in unserem Beispiel eine Abkürzung für /*home/max/ *ist, während die dritte Möglichkeit nur aus dem Homeverzeichnis heraus verwendet werden kann, in dem sich der Ordner *Documents *befindet.

Eine weiter nützliche Abkürzung stellt *".." *dar. Mit *cd .. *gelangt man damit zu dem Übergeordneten Ordner des aktuellen Arbeitsverzeichnisses

#### ls - Verzeichnis auflisten
Um zu sehen, was in dem aktuellen Arbeitsverzeichnis enthalten ist, kann der Befehl *ls *genutzt werden. Er listet alle Unterordner, Dateien und Verlinkungen auf. Für eine übbersichtlichere Darstellung und zusätzliche Informationen kann der Parameter "*-l" *genutzt werden. Hier werden von links nach rechts zu jedem Element die Rechte (siehe Abschnitt Rechte), Besitzer, Gruppenzugehörigkeit (i.d.R. gleichnamig mit Benutzer), Dateigröße, Änderungszeit und Name angezeigt.

#### touch - Datei erstellen
Mit *touch* können einfache Textdateien erstellt werden. *touch *aktuallisiert dabei die Änderungszeit einer Datei und erstellt diese, falls sie nciht existiert.

#### installieren von Programmen über das Terminal
Möchte man Programme nicht über die graphische Oberfläche des Softwarecenters isntallieren, kann man das auch über das Terminal erledigen. Der Befehl dazu lautet:
*sudo apt-get install <programm-name>*

#### neuladen der zu verwendenden Paketquellen
werden neue Paketquellen hinzugefügt oder entfernt, müssen die Einträge neu eingelesen werden. Das ist zum Beispiel der Fall beim Hinzufügen eines neuen Repositories das nicht zu den Standardquellen gehört. Dies geschieht mit Hilfe des Befehls:
*sudo apt-get update*

#### starten von Programmen über das Terminal
Grundsätzlich kann jedes Programm auch über das Terminal gestartet werden. Dafür muss lediglich der Name des Programms als Befehl eingegeben werden. So kann z.B. mit *firefox *der Browser gestartet werden. Dabei kann als Argument direkt die gewünschte URL angegeben werden. So wird mit *firefox ubuntuusers.de *die Seite www.*ubuntuusers.de *geöffnet*. *So lange das gestartete Programm geöffnet wird, kann dabei im Terminal nicht weiter gearbeitet werden. Möchte man nach dem starten eines Programms nicht, dass das Terminal belegt ist, kann man nach dem Befehl ein *& *anhängen um den gestarteten Befehl im Hintergrund zu starten.

Rechte
------
![](./16_17Termin2/ls -l.png)

Linux Betriebssysteme legen großen Wert auf die Rechteverwaltung der Ordner und Datein eines Computers. Bei Änderungen von grundlegenden Systemeinstellungen und der Installation von Programmen werden zum beispiel jedes Mal das Passwort des jeweiligen Benutzers gefragt. Je weiter die gewünschte Veränderung in das System eingreift, desto mehr Privilegien sind von nöten. Die oberste Befehlsgewalt besitzt der sogenannte *root *und ist in Windows in etwa der wohlbekannte *Systemadministrator. *
Die Verwaltung der Rechte und wer, was, mit welchen Dateien machen kann ist zB anhand der Auflistung des *ls -l *Befehls zu sehen. (siehe Abschnitt Terminal) Diese Rechten können unabhängig für jeden Ordner und jede Datei einzeln festgelegt werden. 
Unterschieden wird dabei zwischen dem Besitzer(**u**ser), der Gruppe(**g**roup) und allen Anderen(**o**thers). Diese können Rechte erhalten um Ordern/Dateien zu lesen (engl.: **r**ead), schreiben (engl.: **w**rite) oder auszuführen (engl.: e**x**ecute). 

Rechte können graphisch über den Explorere eingesehen und geändert werden, indem man mit einem Rechtsklick die Eigenschaften(Properties) der gewünschten Datei öffnet und auf dem Reiter Rechte(Permissions) geht.
Im Terminal können die Rechte mit dem Befehl *ls -l * eingesehen werden 

Modifiziert werden können die Rechte im Terminal mit dem Befehl *chmod <Rechte modifizieren> <Dateiname>. *Soll der Datei *test_script.sh *beispielsweise die Rechte zum lesen vom Benutzer und der Gruppe gegeben werden, geschieht das mit dem Befehl *chmod ug+x test_script.sh * mit *chmod o-x *wird allen anderen die Rechte zu Ausführen entzogen.

Weitere Infos zu *chmod* <unterhttps://wiki.ubuntuusers.de/chmod/>

Weitere Infos zu Rechten unter <https://wiki.ubuntuusers.de/Rechte/>

Skripte
-------
Manche Befehle oder Abfolgen von Befehlen, werden so oft benötigt, dass man sich wünschte es gäbe eine Abkürzung dafür. Grundsätzlich ist das möglich mit Skripten. In Skripten können die gleichen Befehle wie auch im Terminal genutzt werden und einfach untereinander, Zeile für Zeile abgespeichert werden. Diese werden dann nacheinander ausgeführt. In der ersten Zeile muss lediglich die sogennante *shebang *eingetragen werden. Mit ihr wird festgelegt, welches Programm genutzt wird im das Skript zu interpretieren. Sie besteht aus *#! *gefolgt von dem Pfad zum gewünschten Interpreter. In der Regel wird /*bin/bash *oder auch /*bin/sh. *Es ist aber auch möglich ein Python-Skript zu schreiben, wofür die *shebang *zu *#!/usr/bin/python *geändert werden muss.


Das fertige Skript kann ausgeführt werden, nachdem die Rechte der Skript-Datei auf auswührbar gesetzt wurde. Entweder mit einem Rechtsklick unter *Rechte *oder mit dem Befehl im Terminal *chmod +x <Skriptname>. *Dafür muss sich das Skript im aktuellen Arbeitsverzeichnis befinden und gegebenenfalls ist die Verwendung des *sudo *Befehls notwendig.

![](./16_17Termin2/script_beispiel.png)

Oben sieht man ein Testskript, dass erst alle Paketquellen aktualisiert und anschließend eventuelle Programmupgrades installiert. Je nach Texteditor, wird beim Speichern der Datei erkannt, dass es sich um ein Sktipt handelt und markiert entsprechende Schlagwörter farbig.

fstab
-----
Die Datei *fstab *ist unter /*etc/ *gespeichert und enthält die Informationen, welche Festplatten und Partitionen zum Systemstart eingebunden werden sollen und mit welchen Optionen. 
Zwar können auch mit dem *mount * Befehl Festplatten und Partitionen über das Terminal eingebunden werden und an Ordner *gebunden *werden, aber dies muss bei jedem Neustart erneut durchgeführt werden. Zudem kann es bei sogannenten *Dualboot-*Systemen ( bei denen mehr als ein Betriebssystem installiert ist die sich Festplatten/Partitionen teilen, zB Windows + Linux ) zu Problemen mit der Rechteverwaltung kommen, wenn Datenträger in einem Dateiformat formatiert sind, das keine Rechteverwaltung unterstützt. So ist die Formatierung NTFS, die Windows i.d.R. verwendet, nicht gut geeignet um Rechte zu Verwalten, so wie es Linux mit der Formatierung *ext2/3/4 *tut. Andersherum kann Windows nicht mit der Formatierung *ext* *umgehen, d.h. Datenträger dieser Formatierung sind unter Windows nicht nutzbar.

 Einträger in *fstab *sind in folgendem Format geschrieben:
<file system> <mount point>   <type>  <options>       <dump>  <pass>



<file system>: 
Was wird eingehängt? Hier kann sowohl ein Pfad wie /*dev/sdX *als auch die die Geräte ID *UUID *verwendet werden. Die Verwendung des Pfads ist aber nicht zu empfehlen, da dieser nicht immer der selbe bleibt. Die *UUID *dagegen ist für jedes Gerät eindeutig und ändert sich nicht. Die *UUID *lässt sich am einfachsten mit dem Programm *gparted *mit einem Rechtsklick auf das gewünschte Gerät in den Informationen nachschauen. *gparted *muss i.d.R. über die standard Paketquellen installiert werden.

<mount point>:
Wohin wird eingehängt? Dieser Ort kann beliebeig gewählt werden. Der Pfad muss aber bereits existieren, d.h. der Ordner in den eingehängt werden soll, muss zunächst erstellt werden und sollte leer sein. Enthaltene Dateien gehen zwar nicht unbedingt verloren, sind aber nicht mehr erreichbar, solange dort etwas eingehängt ist.

<type>:
Wie sieht das aus was eingehängt wird? Bei Festplatten wird hier die jeweilige vorliegende Formatierungsvariante eingetragen. Wird lediglich ein *binding *von Ordner vorgenommen, kann hier *none *eingetragen werden.

<options>:
Wie wird eingehängt? Die Optionen ermöglichen die Kontrolle über die Rechteverwaltung und wer alles ein-/aushängen darf. Für die meisten Fälle reicht hier der Eintrag *defaults. *Treten aber Probleme mit der Rechteverwatlung auf, können zusätzlich mit den Optionen *uid, gid *und *umask *die Besitzer, Gruppen und deren Rechte festgelegt werden. *uid *und *gid *lassen sich im Terminal einfach über *id -u *bzw. *id -g *ermitteln. *umask *enthält die invertierte, octale Darstellung der Rechteverteilung nach dem Schema <user group others> (siehe Rechte). Möchte man beispielsweise die Rechte *rwx r-x --- *festlegen, entspricht das in binärere Darstellung *111 101 000 *und invertiert *000 010 111. *Octal entspricht das *0 2 7 *wie im obigen Beispiel verwendet.

<dump>:
Wird gesichert? Hier kann eine Sicherung eingerichtet werde. Damit haben wir uns aber nicht befasst. Also setzen wir hier eine *0.*

<pass>:
In welcher Reihenfolge wird eingehängt? Hier kann die Reihenfolge des Einhängevorrgangs festgelegt werden. Als erstes müssen der *root- *und *boot-*Ordner eingehängt werden, da diese zum Systemstart notwendig sind (1). Danach können andere Partitionen eingehängt werden, wie die Homeverzeichnisse der Benutzer (2). Am Schluss kommen andere Partitionen wie z.B. Documente Partitionen und der *swap *Bereich in dem z.B. im Ruhezustand Systemdaten hinterlegt werden(0).

 Weiter Infos zu fstab unter <https://wiki.ubuntuusers.de/fstab/>

Verbindung zum u-Account am SCC
-------------------------------

##### Im Terminal
Möchte man sich über das Terminal am SCC anmelden, gelingt das mit dem *ssh *Befehl, gefolgt von u-Kürzel @ SCC-Adresse. 

*ssh u****@student.kit.edu*

beim ersten Verbinden wird der sogenannte Fingerprint des Servers angezeigt und gefragt ob man dieser Verbindung wirklich vertrauen möchte. Der offizielle Fingerprint des Servers kann auf der Website des SCC nachgeschaut werden. <https://www.scc.kit.edu/dienste/4779.php>. Getrennt wird die Verbindung durch den *exit *Befehl.

Sollen nur Dateien herunter- bzw. hochgeladen werden, ist es einfacher mit dem *sftp *oder* scp *Befehl zu arbeiten. Getrennt wird die Verbindung durch den *exit *Befehl.

*sftp u*****@student.kit.edu*

näheres im nächsten Abschnitt.

scp <quelle> <ziel>

z.B.: scp  [@student.[[kit.edu](./student.[[kit.edu.markdown):~/Documents/*]]   ~/Dokumente/SCC_Dokumente
kopiert alle Dateien und Ordner aus dem Ordner *Documents *vom SCC-Server in den lokalen Ordner *SCC_Dokumente *im Dokumente Ordner. "~" steht dabei als Abkürzung für das eigene Homeverzeichnis. 

#### Im Explorer
Über den Explorer kann ebenfalls eine *sftp-*Verbindung zum SCC-Server erstellt werden. Die Vorteile dabei sind zum einen, dass man die gewohnte graphische Oberfläche hat und wie in anderen Ordner auch Datein einfach durch drag&drop Aktionen kopieren und einfügen kann. Zum anderen kann die Verbindung einfach als Lesezeichen gespeichert werden.
Die Verbindung wird entweder erstellt, indem im URL-Adressfeld der Befehl

*sftp:*[u****@student.kit.edu](mailto:u****@student.kit.edu)/home/ws/u****//

eingegeben wird, gefolgt vom eigenen Passwort. Alternativ kann die "Mit Server verbinden ..." Option genutzt werden.

![](./16_17Termin2/scc_verbinden.png)




Lukas
-----

### Sicherheit-Allgemein


* Viren: geringes bis kein Problem unter Linux
* Rechtevergabe: Strenge Richtlinien, damit durch potenzielle Angreifer wenig bis kein Schaden entsteht.
* Programme: Installation aus geprüften Quellen, verwaltet durch den Anbieter der Distribution
* Sicherheitslücken: Auch vorhanden, aber schnelle Fixes durch Community oder Anbieter der Distribution


### Verschlüsselungsmechanismen

1. Verschlüsselung mit distributionseigenem Tool (LUKS+Ext4)
2. Zu beachten:

→ zu verschlüsselndes Medium wird formatiert
→ Festplatte muss bei Installation verschlüsselt werden

* Unter Ubuntu: Suche nach „Disks“/ „Laufwerke“ → Stick/Festplatte auswählen

→ bei Formatieren LUKS+Ext4 auswählen → Passwort eingeben → fertig

* Passwortabfrage kommt jetzt immer wenn das Medium gemountet wird



2. Verschlüsselung mit VeraCrypt
3. VeraCryp nicht in den Quellen von Ubuntu!
4. Erstellen eines verschlüsselten Containers:
	* „Create Volume“ auswählen und der Anleitung folgen (Die ist sehr einfach gehalten und bedarf eigentlich keiner Erklärung)



3. KeePass-Datenbank
4. KeePass erstellt eine Datenbank zur Sicherung von Passwörtern
5. Neue Datenbank kann nur mit Passwort oder auch mit Keyfile gesichert werden
6. Wichtig:

→ Wenn man alle Passwörter in einer Datenbank sichert muss das
Masterpasswort lang und stark sein
→ Keyfile sollte wenn möglich an einem anderen Ort gespeichert sein

* Für neue Passwörter hat KeePass einen Zufallsgenerator



4. SSH
5. Anmeldung via Passwort oder Keyfile
6. Erstellen einer Keyfile und kopieren auf den Server (im Terminal):

→ „ssh-keygen -b 4096“ erstellt eine Keyfile mit einem 4096bit Schlüssel
→ den angegebenen Pfad so belassen
→ Auf Wunsch kann die Datei nochmals mit einem PW verschlüsselt werden

* Nach dem Erstellen auf dem Server einloggen
* im Ordner /home/<user>/.ssh die Datei „authorized_keys“ erstellen mit

„touch authorized_keys“

* jetzt ein zweites Terminal öffnen und den Schlüssel kopieren:

	
``cat /home/<user>/.ssh/id_rsa.pub | ssh <user>@<Server> 'cat >> /home/<user>/.ssh/authorized_keys `` 
(als einen Befehl ins Terminal kopieren. Im Terminal ist STRG+SHIFT+V Einfügen und STRG+SHIFT+C kopieren)


* eventuell muss auf dem Server noch die Datei ``/etc/ssh/sshd_config`` editiert werden (muss vom Systemadmin gemacht werden!)
* genauere Angaben unter:

<https://www.rechenkraft.net/wiki/Root_Server_absichern_(Ubuntu_14.04>)
unter dem Abschnitt: „SSH über Keyfile“

