---
title: engine
id: engine
weight: 30
draft: false
author: "people"
---

## NAME

engine

## SYNOPSIS

get and set the output engine

## USAGE
```
local log = require "lib/dtutils.log"
result = log.engine(level, ...)
```
**level** - _table_ - the log level to get or set the engine for, one of log.debug, log.info, log.warn, log.error
log.success, log.always, log.screen, log.critical  
**...** - _function_ - the output function, one of dt.print, dt.print_error, dt.print_log, print
if not function is included, the current engine is returned for the specified log level

## DESCRIPTION

**engine** returns the output engine for the specified log level if a second argument is not
supplied.  If a function is supplied as the second argment, then the output engine for the specified log level
is set to that.

## RETURN VALUE

**result** - _function_ - the current output engine
