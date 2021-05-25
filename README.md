<div align="center">
<h3>rofi-bluetooth</h3>
<img src="https://github.com/Mysy00/rofi-bluetooth/raw/master/.meta/menu.gif">

`bluetoothctl` `rofi` `dmenu`

</div>

## How dos this fork differ
It almost doesn't differ. I forked it to make it work better with my polybar config (icon for prefix and on/off/dev name to indicate BT status).
Also, with the makefile it's easier to get the script working when using a script to set up your system.

## Installation

1. Install dependencies:
   - [rofi](https://github.com/davatorium/rofi)
   - bluetoothctl (provided by `bluez-utils` in Arch)
2. `git clone https://github.com/Mysy00/rofi-bluetooth.git`
3. `cd rofi-bluetooth`
4. `make install`
5. Make sure ~/.local/bin directory is in your `$PATH`.

### Polybar configuration

```
[module/bluetooth]
type = custom/script
exec = rofi-bluetooth --status
interval = 1
click-left = rofi-bluetooth &

format-prefix = " "
format-prefix-foreground = ${colors.foreground-alt}

```

### BSPWM keybinding

If you're using my dotfiles, you can press `meta+t` to show the menu.

### i3 keybinding

```
bindsym $mod+b exec --no-startup-id rofi-bluetooth
```

### Thanks for the inspiration!

- [firecat53/networkmanager-dmenu](https://github.com/firecat53/networkmanager-dmenu)
- [x70b1's bluetoothctl polybar script](https://github.com/polybar/polybar-scripts/tree/master/polybar-scripts/system-bluetooth-bluetoothctl)
- [ClydeDroid/rofi-bluetooth](https://github.com/ClydeDroid/rofi-bluetooth)
