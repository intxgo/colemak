# XKB config files

## Install system wide:

append new definitions

`cat xkb/symbols/pl >> /usr/share/X11/xkb/symbols/pl`

patch layout list

`patch /usr/share/X11/xkb/rules/evdev.lst xkb/rules/evdev.lst.patch`

`patch /usr/share/X11/xkb/rules/evdev.xml xkb/rules/evdev.xml.patch`


## Set layout from console

`setxkbmap -layout pl -variant polish_colemak`

## Set capslock as shift lock
setxkbmap -option caps:shiftlock

Create a file at ~/.Xmodmap. The file content should be this:

````
! make capslock do shift lock
xmodmap -e "keycode 66 = Shift_Lock"
````

## Macbook keyboard options

```
! ralt become rctrl
setxkbmap -option ctrl:ralt_rctrl

! swap lwin with lctrl
setxkbmap -option altwin:swap_lctrl_lwin
```
