---
title: details
id: details
weight: 10
draft: false
author: "people"
---

# DTUTILS.SYSTEM

## NAME

dtutils.system

## SYNOPSIS

a library of system utilities for use in darktable lua scripts

## USAGE
```
local dtsys = require "lib/dtutils.system"
```
## DESCRIPTION

This library contains routines for interfacing to the operating system from
darktable lua scripts.

## RETURN VALUE

**dtsys** - _library_ - the darktable lua system library

## FUNCTIONS

### [external_command](external_command.md)

pass a command to the operating system for execution and return the result

### [launch_default_app](launch_default_app.md)

open file in default application

### [windows_command](windows_command.md)

pass a command to the windows operating system for execution and return the result

## LICENSE

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 3 of the License, or
(at your option) any later version.
This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.
You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
