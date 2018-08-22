# Termin 2
Created Sonntag 22 November 2015

Live Stick selbst erstellen
---------------------------



Partitionierungsstrategien
--------------------------

![](./Termin_2/pasted_image.png) 

Vorteil von Partitionierung:


* Trennung von Anwendungen/Systemdaten und Nutzerdaten
	* Wenn das System den Geist aufgibt, beeinflusst das die Daten nicht → leichtere Sicherung,


 * Keine Daten doppelt, da jedes Betriebssystem auf den gleichen Speicherort zugreift


![](./Termin_2/pasted_image001.png)


[/mnt/Myfiles/home_clouds/Dropbox/mydropbox/Linuxworkshop/](file:///C:/mnt/Myfiles/home_clouds/Dropbox/mydropbox/Linuxworkshop)


bearbeiten der [/etc/fstab](file:///C:/etc/fstab)

	#Mount Myfiles in /mnt
	UUID=046B17B63B936898   /mnt/Myfiles    ntfs    defaults    0   0
	
	#bind home folders on Myfiles
	/mnt/Myfiles/home_documents    /home/sandro/Dokumente  none    bind 0   0
	/mnt/Myfiles/home_bilder    /home/sandro/Bilder  none    bind 0   0
	/mnt/Myfiles/home_projects   /home/sandro/Projekte  none    bind 0   0
	/mnt/Myfiles/home_videos    /home/sandro/Videos  none    bind 0   0
	/mnt/Myfiles/home_programme    /home/sandro/Programme  none    bind 0   0
	/mnt/Myfiles/home_clouds    /home/sandro/Clouds  none    bind 0   0
	


Alternativprogramme
-------------------


* Installation von Matlab & co. Sudo or not sudo
* ubuntuusers forum


abhängigkeiten: 
python
python3

### Alternativsoftware

<https://wiki.ubuntuusers.de/Software>
<https://wiki.ubuntuusers.de/Grafik>

#### Bild und Videobearbeitung

* gimp
* Pitivi, kdenlive, cinelerra
* weitere....
* darktable

<https://wiki.ubuntuusers.de/pitivi>

es gibt auch eine Eigene Distribution gerade für dieses Thema
<https://ubuntustudio.org/>
Hier würde sich eventuell ein Linux Dualboot empfehlen, damit man diese Distribution bequem  nutzen kann.



* openoffice/libre office
* clipgrab
	* eine menge abhängigkeiten.... siehe ubuntuusers
	* <https://wiki.ubuntuusers.de/Clipgrab>
* Zim
	* Screenshots
	* Tagebuch
	* Gnuplot
	* Codeblock
	* Mindmap
	* Formel einfügen
* octave als alternative zu matlab
* thunderbird


### Backup, Partitionierung

* Partitionierungsstrategie


### Rescue Commands
im allgemeinen ALT+Druck Taste [Sys-Req bzw. S-Abf Taste ]

* "Clean Reboot" ALT+Druck + [reisub] (nacheinander)


STRG+ALT+ F1...F6	 ins Terminal wechseln
STRG+ALT+ F7	 zurück zum X-Server


* xkill - ermöglicht das "töten" eines programms durch einen klick auf das fenster



* Peripheriegeräte



### LinuxMint, Mate, Cinamon, etc....

* KDE
* Gnome
	* GnomeExtensions
* Livestick selbst erstellen



### PDF Manipulation mit der Konsole

<https://wiki.ubuntuusers.de/PDFjam>

pdfjam-slides3up --pagenumbering true --batch folien1.pdf









