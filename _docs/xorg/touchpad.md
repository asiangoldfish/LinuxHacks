---
layout: default
title: Touchpad
parent: Xorg
---

# Touchpad Troubleshooting

Touchpads may have a varying level of support on GNU/Linux systems, depending on the hardware manufacturer, supported drivers and software running on the system. This page proposes a few suggestions to troubleshooting touchpad issues.

## My laptop's touchpad does not work. How to fix it?

Make sure that this isn't only at the operating system level. If possible, boot into the motherboard's UEFI and make sure that the cursor is movable with the touchpad.

If the cursor is movable, the issue is likely related to drivers. Below is a list of possible solutions:

1. Downgrade the Linux kernel.  
    - To check the kernel version, use the command `uname -r`. Instructions on installing a new kernel vary between desktop environments and distributions. Use a search engine to look up instructions for your system.
    - Reboot the system

## Tap-to-click does not work. How to fix it?

Install Xorg's libinput package with your package manager, and make sure that its synaptics package is uninstalled. The packages' names varies between distributions.

| Distribution | Libinput            | Synaptics            |
|:-------------|:--------------------|:---------------------|
| Arch Linux   | xf86-input-libinput | xf86-input-synaptics |

Then, create a new file `40-libinput.conf` in the directory `/etc/X11/xorg.conf.d`. The file's content should look like this:

```sh
Section "InputClass"
    Identifier "touchpad"
    Driver "libinput"
    MatchIsTouchpad "on"
    Option "Tapping" "on"
    Option "NaturalScrolling" "on"
    Option "ClickMethod" "clickfinger"
EndSection
```

If you use a window manager like i3wm, it may be necessary to run a script upon starting up the window manager. There is a git repository with scripts to run upon startup. Execute the following command:

```
git clone https://github.com/maxwell-bland/i3-natural-scrolling-and-tap
```

Then, add the following lines to `~/.config/i3/config`:

```sh
# enable touchpad tap-to-click
exec $HOME/repos/i3-natural-scrolling-and-tap/tap-to-click.sh
```

Now, restart the window manager with `Mod+R`.
