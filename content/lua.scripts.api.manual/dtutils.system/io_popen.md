---
title: io_popen
id: io_popen
weight: 50
draft: false
author: "people"
---

## NAME

io_popen

## SYNOPSIS

wrapper around the lua io.popen function

## USAGE
```
local dsys = require "lib/dtutils.system"
local result = dsys.io_popen(command)
```
**command** - _string_ - a command to execute and attach to

## DESCRIPTION

io_popen wraps the lua io.popen system call to provide
correct sanitization of windows commands

## RETURN VALUE

see the lua io.popen documentation
