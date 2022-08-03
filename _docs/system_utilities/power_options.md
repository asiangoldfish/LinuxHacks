---
layout: default
title: Power Options
parent: System Utilities
---

# Power Options

## System Suspension

Overview on different methods to suspend the system. The methods' success vary depending on the hardware and init system.

| Description | Command |
|:------------|:--------|
| Generic command for system suspension | `sudo sh -c "echo mem > /sys/power/state"` |
| System suspension with systemd | `systemctl suspend` |

## Systemd services

Using systemd's services, commands may be executed before or after the computer has entered a certain stage. While desktop environments like KDE and GNOME locks the user session before the system suspends, sleeps or hibernates, this feature is not included in minimalistic systems like window managers. A workaround for this is to manually setup the screenlock system.


### Betterscreenlock

Github: [https://github.com/betterlockscreen/betterlockscreen](https://github.com/betterlockscreen/betterlockscreen)

Betterscreenlock is a Bash script and and is exclusively for the i3wm. It's a i3block wrapper and aims to solve the problem with the 2-3 secnods startup delay. Its installation instructions are found in its Github repository.

**Note**: Users have had varying results from editing the following line in `/etc/systemd/system/betterlockscreen@.service`:

```ini
Type: simple
```

If the script does not successfully execute after waking up the machine, then edit the above line to the following:

```ini
Type: forking
```

