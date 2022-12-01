---
layout: default
title: Linux Commands
has_children: true
---

# Files

This category is designated for file related applications, commands and tools.

Most shells in Unix and Unix-like operating systems offer similar commands for managing files. An overview over these commands are found below:

| Commands                                  | Description                       |
|:------------------------------------------|:----------------------------------|
| `cp path/to/source path/to/target`        | Copy file                         |
| `find $DIRNAME -name $PATTERN`            | Find file                         |
| `less`                                    |                                   |
| `mkdir DIRNAME`                           | Create new directory              |
| `rm path/to/file`                         | Delete file                       |
| `rm -f path/to/file`                      | Delete forcefully                 |
| `rm -r path/to/directory`                 | Delete directory recursively      |
| `rmdir path/to/directory`                 | Delete empty directory            |
| `mv path/to/source path/to/target`        | Move file/directory               |
| `tail`                                    |                                   |
| `touch FILENAME`                          | Create new file                   |
| `entr`                                    | Mimic keyboard actions            |

## Progression Bar
There is a patch for the `cp` and `mv` commands that adds a progession bar. To
patch the commands, follow along this tutorial: [Advanced Copy – Add Progress Bar To cp And mv Commands In Linux](https://ostechnix.com/advanced-copy-add-progress-bar-to-cp-and-mv-commands-in-linux/)

# Entr
| Commands                                  | Description                                        |
|:------------------------------------------|:---------------------------------------------------|
| `ls \| entr SOME_COMMAND`                 | Execute named commands whenever a file has changed |

# Navigation Commands

| Commands                                 | Description                        |
|:-----------------------------------------|:-----------------------------------|
| `cd`                                     | Change working directory           |
| `ls`                             | List content of current working directory  |
| `pwd`                               | Print name of current working directory |


