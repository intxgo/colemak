# XKB config files

## Install system wide:

append new definitions

`cat xkb/symbols/pl >> /usr/share/X11/xkb/symbols/pl`

patch layout list

`patch /usr/share/X11/xkb/rules/evdev.lst xkb/rules/evdev.lst.patch`

`patch /usr/share/X11/xkb/rules/evdev.xml xkb/rules/evdev.xml.patch`


## Set layout from console

`setxkbmap -layout pl -variant polish_colemak`
