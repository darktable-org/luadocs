---
title: external_command
id: external_command
weight: 20
draft: false
author: "people"
---

## NAME

external_command

## SYNOPSIS

pass a command to the operating system for execution and return the result

## USAGE
```
local dsys = require "lib/dtutils.system"
local result = dsys.external_command(command)
```
**command** - _string_ - a string containing the command and arguments to be passed to the operating system for execution.

## DESCRIPTION

**external_command** passes a command to the operating system for execution and returns the results.

## RETURN VALUE

**result** - _number_ = the return value signalling success or failure.
