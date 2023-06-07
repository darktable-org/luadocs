---
title: troubleshooting
id: troubleshooting
weight: 30
draft: false
author: "people"
---

Running darktable with Lua debugging enabled provides more information about what is occurring within the scripts.

### Snap

Open a terminal and start darktable with the command `snap run darktable -d lua`. This provides debugging information to give you insight into what is happening.

### Linux

Open a terminal and start darktable with the command `darktable -d lua`. This provides debugging information to give you insight into what is happening.

### MacOS

Open a terminal and start darktable with the command `/Applications/darktable.app/Contents/MacOS/darktable -d lua`. This provides debugging information to give you insight into what is happening.

### Windows

Open a command prompt. Start darktable with the command `"C:\Program Files\darktable\bin\darktable" -d lua > log.txt 2> log_err.txt`. `stdout`, which contains regular output of commands like `print()` will get printed into the `log.txt` file. `stderr`, which contains program errors will get saved inside `log_err.txt` file. This provides debugging information to give you insight into what is happening.
