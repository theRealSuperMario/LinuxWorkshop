# USB Sticks erstellen
Created Dienstag 10 November 2015

Über Startmedienersteller
-------------------------


Image mit DD kopieren
---------------------

![](./USB_Sticks_erstellen/pasted_image.png)

![](./USB_Sticks_erstellen/pasted_image001.png)

![](./USB_Sticks_erstellen/pasted_image002.png)

für eine Fortschrittsanzeige wird pv benötigt
→ sudo apt-get install pv

	dd if=/dev/sdb of=/dev/sdc bs=1M #ohne Progress bar
	
	dd if=/dev/urandom | pv | dd of=/dev/null #mit Progressbar
	
	sudo fdisk -l	#alle devices anzeigen lassen
	
	#vorher universe aktivieren!!
	#installation von gnome
	sudo apt-get install gnome-core


	#!/bin/bash
	
	sudo apt-get update
	sudo apt-get upgrade
	sudo apt-get install gnome-core
	
	#kleines Skript zum erstellen der sticks.
	#es muss 3 mal eingabe gedrückt werden, u.A. um den display manager auszuwählen



Desktop Umgebungen
------------------

für den Workshop Ubuntu installieren und dann gnome desktop nachinstallieren


<https://wiki.ubuntuusers.de/GNOME_Installation>

sudo apt-get install gnome	



<http://wiki.ubuntuusers.de/desktop>

<http://www.tecmint.com/install-kde-plasma-5-in-linux/>


