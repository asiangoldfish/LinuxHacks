---
layout: default
title: Bash
parent: Shells
has_toc: true
---

# Bash

***Table of Content***
  - [Documentation](#documentation)
  - [Overview](#overview)
  - [Detect A Sourced Script](#detect-a-sourced-script)
  - [Strings](#strings)

## Documentation
Bash documentations come in different formats. Use the table below to find the appropriate format for you.

| Format | Link |
|:-------|:-----|
| HTML | [gnu.org](https://www.gnu.org/software/bash/manual/bash.html){: .btn .btn-blue } |
| PDF | [gnu.org](https://www.gnu.org/software/bash/manual/bash.pdf){: .btn .btn-blue } |
| Manpages | [linux.die.net](https://linux.die.net/man/1/bash){: .btn .btn-blue } |

## Overview
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

## Detect A Sourced Script
```sh
[[ $_ != $0 ]] && echo "Script is being sourced" || echo "Script is a subshell"
```

Source: https://stackoverflow.com/a/2687092

## Strings
***Split Strings***
Strings in bash can be split by a delimiter `IFS`:

```sh
IFS="=" read -ra array <<< "$arg"
```

In the example above,

- `=` is the symbol to delimiter. This is what the string will be split by
- `$arg` is the string to split
- `read -ra array` will read the string into the array array variable

## Arrays
***Whether An Array Has A Given Element***

```sh
if [[ " ${array[*]} " =~ " ${value} " ]]; then
    # whatever you want to do when array contains value
fi

if [[ ! " ${array[*]} " =~ " ${value} " ]]; then
    # whatever you want to do when array doesn't contain value
fi
```

Disclaimer: In cases where the value you are searching for is one of the words in an array element with spaces, it will give false positives. Example
```sh
array=("Jack Brown")
value="Jack"
```
Source: [stackoverflow.com](https://stackoverflow.com/a/15394738)

***Find Array Length***

```sh
array=( "foo" )
length="${#array[@]}"
```

***Last Element In Array***
```sh
array=( "foo" )
length="${#array[@]}"
element="${array[$length - 1]}"
```