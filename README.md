# dwm - samin's fork
---

*dwm is an extremely fast, small, and dynamic window manager for X.*

## Patches used in this fork

- pertag
- AlwaysCenter
- HideVacant tags
- UnderlineTags (to hide that annoying little box on tags)
- xrdb (i cant look at same color every day nd im too lazy to rebuild)

## Config changes

- font used Bitstream NF
- underline tags configs are all 0
- mod key mapped  to super key
- super+shift_end => exit out of x session
- super+q ==> quit active window

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
