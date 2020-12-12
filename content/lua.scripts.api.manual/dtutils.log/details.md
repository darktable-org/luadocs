---
title: details
id: details
weight: 10
draft: false
author: "people"
---

## NAME

dtutils.log

## SYNOPSIS

darktable lua logging library

## USAGE
```
local log = require "lib/dtutils.log"
```
## DESCRIPTION

**log** provides a multi-level logging solution for use with
the darktable lua scripts.  With this library you can leave log messages 
scattered through out your code and only turn them on as necessary.

## RETURN VALUE

**log** - _library_ - the darktable lua logging functions

## FUNCTIONS

### [caller](caller.md)

get the name and line number of the calling routine

### [engine](engine.md)

get and set the output engine

### [log_level](log_level.md)

get or set the log level

### [msg](msg.md)

print a log message

## EXAMPLE
```
local log = require "lib/dtutils.log"
local cur_level = log.log_level()
log.log_level(log.warn)
```
print out warning, error and success messages as code is running
```
log.log_level(debug)
```
print out debugging messages too because this isnt working
```
log.log_level(info)
```
I want to make sure this is working ok
```
log.log_level(cur_level)
```
reset the logging level back to normal

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
