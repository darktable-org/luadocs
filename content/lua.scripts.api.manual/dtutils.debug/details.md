---
title: details
id: details
weight: 10
draft: false
author: "people"
---

## NAME

dtutils.debug

## SYNOPSIS

debugging helpers used in developing darktable lua scripts

## USAGE
```
require "lib/dtutils.debug"
```
## DESCRIPTION

dtutils.debug provides an interface to the darktable debugging routines.

## RETURN VALUE

**dd** - _library_ - the darktable lua debugging helpers

## FUNCTIONS

### [dprint](dprint.md)

pass a variable to darktable.debug.dump and print the results to stdout

### [new_tracepoint](new_tracepoint.md)

create a function returning a tracepoint

### [terse_dump](terse_dump.md)

set darktable.debug.known to shorten all image dumps to a single line

### [tracepoint](tracepoint.md)

print out a tracepoint and dump the arguments

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

