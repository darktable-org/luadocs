---
title: check_if_bin_exists
id: check_if_bin_exists
weight: 20
draft: false
author: "people"
---

## NAME

check_if_bin_exists

## SYNOPSIS

check if an executable exists

## USAGE
```
local df = require "lib/dtutils.file"
local result = df.check_if_bin_exists(bin)
```
**bin** - _string_ - the binary to check for

## DESCRIPTION

**check_if_bin_exists** checks to see if the specified binary exists.
**check_if_bin_exists** looks for an executable in the following order:

* If an executable preference is registered, then it's checked to make sure it's a file, exists, and is executable. If it passes all these tests it is returned to the caller. On non-windows operating systems a windows binary can be specified and the wine installation will be checked for the executable.

* If an executable preference doesn't exist or a test fails then an attempt is made to find the file in an operating system specific manner:
  * unix or linux
    * the user's path is checked for a matching binrary using the which command
  * macos
    * first the user's path is checked for a matching binrary using the which command
    * if the executable isn't found a search of the _/Applications_ directory is performed
  * windows
    * the user's path is checked using the where command
    * if the executable isn't found, then _C:\\Program Files_ is searched for the executable 
    * if the executable isn't found, then _C:\\Program Files \(x86\)_ is searched

## RETURN VALUE

**result** - _string_ - the sanitized path of the binary, false if not found

## LIMITATIONS

* it still can't find GIMP on windows.  GIMP on windows is installed in C:\\Program Files\\GIMP 2\\bin\\gimp-2.10.exe, if you use the installer from www.gimp.org.  When **check_if_bin_exists** searches for GIMP it looks for gimp.exe.  If the search was for gimp\*exe then things like gimptool, gimp-debug-tool, gimp-console, etc. are found.  Depending on who packaged gimp,there is an executable called gimp.exe which satisfies the search but is a GIMP launcher that exits immediately so the script returns and the image is not edited. Therefore, if you are a windows user, then you need to specify the location of the GIMP executable either from the [Edit with GIMP](../../../lua.scripts.manual/scripts/contrib/gimp.md) script or using [executable manager](../../../lua.scripts.manual/scripts/tools/executable_manager.md).

* flickering windows - on windows every command must run in a window, so every time a script uses a system command a window is opened, the command is run, and the window is closed  checking for a binary needs multiple system commands to find the file and then check it which causes "flickering windows".  If the flickering windows is too disturbing a lua preference is available in the settings to use the old check_if_bin_exists\(\).  The old check_if_bin_exists\(\) still causes flickering windows but it's much less.  The downside is that no searching is performed so the user has to specify the location of all executables.


## CHANGELOG

20201225 - Added search capability and file checking to ensure it's an executable - Merry Christmas
