---
title: sanitize
id: sanitize
weight: 40
draft: false
author: "people"
---

## NAME

sanitize

## SYNOPSIS

surround a string in quotes making it safe to pass as an argument

## USAGE
```
local ds = require "lib/dtutils.string"
local result = ds.sanitize(str)
```
**str** - _string_ - the string that needs to be made safe

## DESCRIPTION

**sanitize** converts a string into a version suitable for
use passing as an argument in a system command.

## RETURN VALUE

**result** - _string_ - a websafe string
