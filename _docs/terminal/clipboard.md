---
layout: default
title: Clipboard
has_children: true
---

# Clipboard

## Xsel
This application lets the user manipulate the X selection. To copy stdin to clipboard, use the following command:

```sh
echo "foo" | xsel -b -i
```

`-b` tells xsel to write to the clipboard, while `-i` makes xsel read from stdin.


