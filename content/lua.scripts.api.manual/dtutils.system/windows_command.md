---
title: windows_command
id: windows_command
weight: 40
draft: false
author: "people"
---

## NAME

windows_command

## SYNOPSIS

pass a command to the windows operating system for execution and return the result

## USAGE
```
local dsys = require "lib/dtutils.system"
local result = dsys.windows_command(command)
```
**command** - _string_ - a string containing the command and arguments to be passed to the operating system for execution.

## DESCRIPTION

The normal method of executing an operating system command is using dt.control.execute(), but that doesn't 
work with Windows when more than one item in the command is quoted.  In order to ensure command execution on Windows we 
create a batch file in the temporary directory, put the command in it, execute the batch file, then return the result.

## RETURN VALUE

**result** - _number_ - the return value signalling success or failure.
