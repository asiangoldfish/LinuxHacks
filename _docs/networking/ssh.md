---
layout: default
title: Secure Shell
parent: Networking
---

# Secure Shell

ssh (SSH client) is a program for logging into a remote machine and for executing commands on a remote machine.  It is intended to provide secure encrypted communications between two untrusted hosts over an insecure network.  X11 connections, arbitrary TCP ports and UNIX-domain sockets can also be forwarded over the secure channel.

To get started, open the terminal and enter the following command:

```sh
ssh HOST@HOSTNAME
```

where the `HOST` is the account username and `HOSTNAME` is the domain name, host name or IP-address. Example:

```sh
ssh foo@example.com
```