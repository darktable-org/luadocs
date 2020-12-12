---
title: caller
id: caller
weight: 20
draft: false
author: "people"
---

## NAME

caller

## SYNOPSIS

get the name and line number of the calling routine

## USAGE
```
local log = require "lib/dtutils.log"
result = log.caller(level)
```
**level** - _number_ - the  number of stack levels to go down to retrieve the caller routine information

## DESCRIPTION

**caller** gets the name and line number of the calling routine and returns it

## RETURN VALUE

**result** - _string_ - the name and line number of the calling function or 'callback: ' if the attempt to get the caller returns nil
