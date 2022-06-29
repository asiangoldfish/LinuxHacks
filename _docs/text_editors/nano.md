---
layout: default
title: Nano
parent: Text Editors
---

# Nano

## Nano Configuration
Nano's config file exists in two location: in user home directory as "~/.nanorc" or system-wide as "/etc/nanorc". To get started, copy the system-wide config to the home directory:

```
cp /etc/nanorc ~/.nanorc
```

This template file includes a list of options and are also explained. It acts as a good starting point to explore what some of the options Nano's config offers. A simplified starting point can be found [here](https://github.com/asiangoldfish/configspack/blob/main/nanorc).

[CouldBeThis](https://github.com/CouldBeThis/nano-configs) has a [collection of syntax definitions] to bring some colours to the text editor. To include these, do the following steps:
- Follow the installation steps in the readme document
- The `install.sh` script creates a new `.nanorc` file in the home directory. Overwrite this document with the following code:
  ```sh
  # Include syntax definitions
  include "~/.nano/*.nanorc"
  ```
  This simplifies the code.

To implement syntax definitions system wide, move them to `/usr/share/nano/`.
```
sudo cp ~/.nano/*.nanorc" /usr/share/nano/
```