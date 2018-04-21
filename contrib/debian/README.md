
Debian
====================
This directory contains files used to package carebitcoind/carebitcoin-qt
for Debian-based Linux systems. If you compile carebitcoind/carebitcoin-qt yourself, there are some useful files here.

## carebitcoin: URI support ##


carebitcoin-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install carebitcoin-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your carebitcoinqt binary to `/usr/bin`
and the `../../share/pixmaps/carebitcoin128.png` to `/usr/share/pixmaps`

carebitcoin-qt.protocol (KDE)

