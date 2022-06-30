---
layout: default
title: Systemd
parent: System Utilities
---

# Systemd

More about systemd: [systemd.io](https://systemd.io/)

## Managing Services

Replace `[process]` with the actual process to manage

| Description               | Command                           |
|:--------------------------|:----------------------------------|
| Check service status      | `systemctl status [process]`      |
| Start service             | `sudo systemctl start [process]`  |
| Stop service              | `sudo systemctl stop [process]`   |
| Enable service on startup | `sudo systemctl enable [process]` |
| Disable service on startup| `sudo systemctl disable [process]`|
