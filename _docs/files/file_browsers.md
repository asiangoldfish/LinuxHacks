---
layout: default
title: File Browsers
parent: Files
---

# File Browsers

## Ranger
Exit Ranger and automatically change directory to pwd in Ranger:  
`alias ranger='ranger --choosedir=$HOME/.rangerdir; LASTDIR=`cat $HOME/.rangerdir`; cd "$LASTDIR"'`
