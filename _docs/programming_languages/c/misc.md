---
layout: default
title: Miscellaneous
parent: C
---

# Clear Screen
C does not have the concept of C and therefore there are portable methods to clear the console screen. There are; however, workaround methods:

**Method 1:**
`printf("\e[1;1H\e[2J");` works only on ANSI terminals on POSIX compliant terminal emulators.

