---
title: is_not_sanitized
id: is_not_sanitized
weight: 30
draft: false
author: "people"
---

## NAME

is_not_sanitized

## SYNOPSIS

Check if a string has been sanitized

## USAGE
```
local ds = require "lib/dtutils.string"
local result = ds.is_not_sanitized(str)
```
**str** - _string_ - the string that needs to be made safe

## DESCRIPTION

**is_not_sanitized** checks a string to see if it
has been made safe use passing as an argument in a system command.

## RETURN VALUE

**result** - _boolean_ - true if the string is not sanitized otherwise false
