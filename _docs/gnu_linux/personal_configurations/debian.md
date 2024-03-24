---
layout: default
title: Debian
parent: Personal Configurations
grand_parent: GNU / Linux
---

# Debian
[My configurations](https://github.com/asiangoldfish/neovim-config) includes a [post-installation script](https://github.com/asiangoldfish/neovim-config/blob/main/postinstall_scripts/debian.sh) for Debian and Debian-based distributions. It's based on [Debian stable](https://www.debian.org/releases/stable/) (bookworm), which means some packages are outdated. To combat this, the script will instead build these packages from source. In some situations, package versions and available differ across distributions. In this case, `uname` is used to identify the distribution name.

*Disclaimer:* I am the only maintainer of the post-installation script and as a result, the script may break. This is simply because the script is suited to my own needs. If you use it for yourself, it's your own responsibility to ensure it works for you, and executing the script is at your own risk. *Always read scripts and validate them before execution. Scripts may be harmful*.

## Installation
Read the [instructions on GitHub](https://github.com/asiangoldfish/neovim-config/blob/main/docs/post-installations.md) to learn how to execute the script.
