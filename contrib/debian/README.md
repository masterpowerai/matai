
Debian
====================
This directory contains files used to package masterpoweraid/masterpowerai-qt
for Debian-based Linux systems. If you compile masterpoweraid/masterpowerai-qt yourself, there are some useful files here.

## masterpowerai: URI support ##


masterpowerai-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install masterpowerai-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your masterpowerai-qt binary to `/usr/bin`
and the `../../share/pixmaps/masterpowerai128.png` to `/usr/share/pixmaps`

masterpowerai-qt.protocol (KDE)

