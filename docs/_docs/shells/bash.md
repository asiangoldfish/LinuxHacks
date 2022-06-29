---
layout: default
title: Bash
parent: Shells
---

# Bash

One of the most commonly used shell command languages and the default shell in most popular Linux distributions.

User customizations are commonly found in .bashrc. The full path is: "/home/username/.bashrc". If the user is root, then the full path is: "/root". Creating a new user may not include a new home directory, in which case Bash doesn't setup customization options for you. To do this, do the following:
- Create a new home directory and transfer its ownership to the new user (assuming that you're the root user)
  ```sh
  cd /home
  mkdir username  # The new user's username
  chown username:username username
  cd username
  ```
- Create ".bash_profile" using `touch .bash_profile` and use your favourite editor to append the following code:
  ```sh
  if [ -f ~/.bashrc ]; then
      source ~/.bashrc
  fi
  ```

To read about the difference between ".bash_profile" and ".bashrc", and to learn more about them, read [here](https://linuxize.com/post/bashrc-vs-bash-profile/)

This post from [Stack Overflow](https://stackoverflow.com/questions/9953005/should-the-bashrc-in-the-home-directory-load-automatically/9954208#9954208) explains the order of which Bash loads configuration files.

Bash is extremely customizable. [Here](https://github.com/asiangoldfish/configspack/blob/main/bashrc) is a starting point.
