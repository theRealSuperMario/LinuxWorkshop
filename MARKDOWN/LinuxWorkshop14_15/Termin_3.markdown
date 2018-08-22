# Termin 3
Created Donnerstag 26 November 2015

Alternativprogramme
-------------------

* octave
* latex editor: kile
	* __sehr empfehlenswert__
* latex distribution: texlive

<https://wiki.ubuntuusers.de/LaTeX>

* XBMC [neuerdings KODI]

<http://kodi.tv/download/>
<https://wiki.ubuntuusers.de/Kodi>

* Stand 26.11.15: stable release:15.x Isengard
* leider etwas komplizierter für neuere versionen [14.10 aufwärts]
* lieber einfach sudo apt-get install xbmc [version 14.x]




![](./Termin_3/pasted_image001.png)

sudo apt-get update nicht vergessen!!!!


* kodi kann auch als "standalone" programm laufen [z.B. auf raspberry pi]
* es gibt eigene distributionen dafür
	* osmc
	* raspbmc
	* open elec
	* .....


### Windowsprogramme mit WINE benutzen
Wine is not an emulator [WINE]


* kompatibilitätscheck über <https://appdb.winehq.org/>
* <https://wiki.ubuntuusers.de/Wine>


![](./Termin_3/pasted_image.png)

bsp. LT Spice

### Virtuel Box

nicht vergessen die gasterweiterungen zu installieren !!!
sonst keine gemeinsamen ordner, copy paste und drag n drop möglich 

![](./Termin_3/pasted_image002.png)


Um an die Gasterweiterungen zu gelangen, muss erst eine VM installiert werden [z.B. Windows 7]
dann Geräte → Medium mit GAsterweiterungen einlegen 


Konsole
-------

* pdftk
* pdfjam
* bin/bash




KDE
---

### (un)installation
<http://ubuntuhandbook.org/index.php/2015/08/install-kde-plasma-plasma-5-4/>

sudo add-apt-repository ppa:kubuntu-ci/stable
sudo apt-get update	[!!!!]
sudo apt-get install plasma-desktop

uninstall:
sudo apt-get install ppa-purge && sudo ppa-purge ppa:kubuntu-ci/stable




### Features

* ALT+Leerzeichen
* sieht toll aus
* konsole im dateibrowser integriert
	* dateibrowser heißt dolphin
	* F4 in dolphin öffnet konsole
* Mausgesten
* Desktop widgets
* viele personalisierungsfunktionen


### Eigene KDE Programme

* Amarok: Musik Wiedergabe [itunes ersatz]


