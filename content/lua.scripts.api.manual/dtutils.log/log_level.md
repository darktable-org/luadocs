---
title: log_level
id: log_level
weight: 40
draft: false
author: "people"
---

## NAME

log_level

## SYNOPSIS

get or set the log level

## USAGE
```
local log = require "lib/log"
local result = log.log_level(...)
```
**...** - _arguments_ - if none is supplied, then the current log level is returned as one of:
log.debug, log.info, log.warn, log.error, log.success.  If one of log.debug, log.info, log.warn,
log.error, or log.success is supplied as the argument then the log level is set to that value.  All
log levels greater than or equal in value will be enabled.  Any levels of lesser value will be disabled.

## DESCRIPTION

**log_level** gets and sets the logging level.  When called with no arguments the current log level
is returned as one of log.debug, log.info, log.warn, log.error, or log.success.  When called with one of log.debug, 
log.info, log.warn, log.error or log.success then the log level is set.  When setting the log level all levels 
equal or greater are enabled and any of lesser value are disabled.  See the example.

## RETURN VALUE

**result** - _log level_ - one of log.debug, log.info, log.warn, log.error or log.success

## EXAMPLE

Assume that the current log level is log.error.  Calling 
```
log.log_level()
```
 will return log.error.
Calling 
```
log.log_level(log.info) 
```
will leave log.debug disabled, and enable log.info, log.warn, log.error and 
log.success.  log.info will be returned as the log_level.
