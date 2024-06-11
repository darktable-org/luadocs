---
title: os_execute
id: os_execute
weight: 60
draft: false
author: "people"
---

## NAME

os_execute

## SYNOPSIS

wrapper around the lua os.execute function

## USAGE
```
local dsys = require "lib/dtutils.system"
local result = dsys.os_execute(command)
```
**command** - _string_ - a command to execute n the operating system

## DESCRIPTION

os_execute wraps the lua os.execute system call to provide
correct sanitization of windows commands

## RETURN VALUE

see the lua os.execute documentation
