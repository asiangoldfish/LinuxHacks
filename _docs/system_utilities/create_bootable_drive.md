---
layout: default
title: Create Bootable Drive
parent: System Utilities
---

# Create Bootable USB Drive
## Windows  
[WoeUSB](https://github.com/WoeUSB/WoeUSB) is a tool to create a bootable flash drive media for Windows systems. Download the application from the [WoeUSB repository](https://github.com/WoeUSB/WoeUSB) and use the following commands where the .bash file was downloaded to:
```
chmod +x path/to/woeusb-N.N.N.bash
sudo bash path/to/woeusb-N.N.N.bash --devices win.iso /dev/sdX  # win.iso is the Windows iso file, and sdX is the file representing the flash drive
```
**Disclaimer:** The application does not prompt you to confirm this action. Please ensure that the file and drive are correct.
**Disclaimer:** The process may take a long time. It may seem to hault, but is actually doing work in the background.