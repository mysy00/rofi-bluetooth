<div align="center">
<h3>rofi-bluetooth</h3>
<img src="https://github.com/Mysy00/rofi-bluetooth/raw/master/.meta/menu.gif">

`bluetoothctl` `rofi` `dmenu`

</div>

## Installation

1. Install dependencies:
  - [rofi](https://github.com/davatorium/rofi)
  - bluetoothctl (provided by `bluez-utils` in Arch)
1. `git clone https://github.com/Mysy00/rofi-bluetooth.git`
1. `cd rofi-bluetooth`
1. `make install`
1. Make sure ~/.local/bin directory is in your `$PATH`.

### Polybar configuration

```
[module/bluetooth]
type = custom/script
exec = rofi-bluetooth --status
interval = 1
click-left = rofi-bluetooth &

format-prefix = " "

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
