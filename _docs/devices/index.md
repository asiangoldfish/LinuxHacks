---
layout: default
title: Devices
has_children: true
---

# Devices

is a lookup-page for device-related subjects.

## Touchpad
[Back to top](#top)

```

# Match on all types of devices but joysticks
#
# If you want to configure your devices, do not copy this file.
# Instead, use a config snippet that contains something like this:
#
# Section "InputClass"
#   Identifier "something or other"
#   MatchDriver "libinput"
#
#   MatchIsTouchpad "on"
#   ... other Match directives ...
#   Option "someoption" "value"
# EndSection
#
# This applies the option any libinput device also matched by the other
# directives. See the xorg.conf(5) man page for more info on
# matching devices.


Section "InputClass"
	Identifier "touchpad"
	Driver "libinput"
		MatchIsTouchpad "on"
		Option "Tapping" "on"
		Option "NaturalScrolling" "on"
		#Option "ClickMethod" "clickfinger"
		Option "TapButtonMap" "lrm"
		Option "ScrollMethod" "twofinger"
EndSection
```