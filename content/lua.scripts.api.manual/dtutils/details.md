---
title: details
id: details
weight: 10
draft: false
author: "people"
---


## NAME

dtutils

## SYNOPSIS

A Darktable lua utilities library

## USAGE
```
local du = require "lib/dtutils"
```
## DESCRIPTION

**dtutils** provides a common library of functions used to build
lua scripts.

## RETURN VALUE

**du**- _library_ - the library of functions

## FUNCTIONS

### [check_min_api_version](check_min_api_version.md)

check the minimum required api version against the current api version

### [check_os](check_os.md)

check that the operating system is supported

### [join](http://github.com/darktable-org/lua-scripts/wiki/join.md)

join a table of strings with a specified separator

### [prequire](http://github.com/darktable-org/lua-scripts/wiki/prequire.md)

a protected lua require

### [spairs](http://github.com/darktable-org/lua-scripts/wiki/spairs.md)

an iterator that provides sorted pairs from a table

### [split](http://github.com/darktable-org/lua-scripts/wiki/split.md)

split a string on a specified separator

## SEE ALSO

[dtutils.debug](../dtutils.debug/details.md), [dtutils.file](../dtutils.file/details.md), [dtutils.log](../dtutils.log/details.md), [dtutils.string](../dtutils.string/details.md), [dtutils.system](../dtutils.system/details.md)

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

## COPYRIGHT

Copyright (C) 2016 Bill Ferguson <wpferguson@gmail.com>.  
Copyright (C) 2016 Tobias Jakobs
