---
layout: default
title: Network Drivers
parent: Networking
---

# Network Drivers

Propriatary drivers may not be installed by default. This can cause a headache, because you need internet connection before even installing anything. Here are some tips that can help solving this issue:

* Connect the system to a router/switch with an Ethernet cable.
* Connect a smartphone to the internet and use it as a mobile hotspot. If limitations on mobile data is an issue, then be sure to first install the network card drivers before anything else.
* Share the smartphone's internet connection with your system using a USB cable, if your phone supports this.

## Intel
Available drivers for Intel Network Cards: [Intel Support](https://www.intel.com/content/www/us/en/support/articles/000005511/wireless.html)

| Distribution | Commands |
|:-------------|:---------|
| Debian | `sudo apt update && sudo apt install iwlwifi` |