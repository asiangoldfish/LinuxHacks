---
layout: default
title: File Conversions
parent: File Management
grand_parent: GNU / Linux
---

# PDF To Plain Text

Convert a PDF file to plain text.

```sh
pdftotext foo.pdf bar.txt
```


# PPTX to PDF

Quickly batch convert Microsoft PowerPoint Open XML (PPTX) to Portable Document Format (PDF) files.

System requirements: `libreoffice`

```sh
cd path/to/source
libreoffice --headless --invisible —convert-to pdf *.pptx
```