---
title: msg
id: msg
weight: 50
draft: false
author: "people"
---

## NAME

msg

## SYNOPSIS

print a log message

## USAGE
```
local log = require "lib/log"
log.msg(level, ...)
```
**level** - _table_ - the type of message, one of: 
- log.debug    - debugging messages
- log.info     - informational messages
- log.warn     - warning messages 
- log.error    - error messages 
- log.success  - success messages
- log.always   - an internal message for debugging
- log.screen   - output 1 line of text to the screen
- log.critical - print a critical message to the console  

**...** - _string(s)_ - the message to print, which could be a comma separated set of strings

## DESCRIPTION

**msg** checks the level to see if it is enabled, then prints the level type and message if it is.
Messages are output using the engine configured in each log level.

## LIMITATIONS

If you use log.msg in a callback, the name of the calling routine can't be determined.  A solution
is to include some means of reference such as the name of the callback as an argument, i.e. 
```
log.msg(log.debug, "libPlugin.format_combobox:", "value is " .. self.value)
```
which would result in
```
DEBUG: callback: libPlugin.format_combobox: value is JPEG
```
