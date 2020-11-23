# Dwn
Dwm is an extremely fast, small, and dynamic window manager for X.

## Patches
+ [fullgaps](https://dwm.suckless.org/patches/fullgaps/): This patch adds gaps between client windows.
+ [hide_vacant_tags](https://dwm.suckless.org/patches/hide_vacant_tags/): This patch prevents dwm from drawing tags with no clients (i.e. vacant) on the bar.
+ [noborder](https://dwm.suckless.org/patches/noborder/): Remove the border when there is only one window visible.
+ [pertag](https://dwm.suckless.org/patches/pertag/): This patch keeps layout, mwfact, barpos and nmaster per tag.
+ [systray](https://dwm.suckless.org/patches/systray/): A simple system tray implementation.

## Shortcuts
// TODO

Requirements
------------
In order to build dwm you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install


Running dwm
-----------
Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 exec dwm

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm


Configuration
-------------
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.
