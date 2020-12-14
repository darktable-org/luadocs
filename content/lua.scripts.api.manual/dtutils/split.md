---
title: split
id: split
weight: 70
draft: false
author: "people"
---

## NAME

split

## SYNOPSIS

split a string on a specified separator

## USAGE
```
local du = require "lib/dtutils"
local result = du.split(str, pat)
```
**str** - _string_ - the string to split  
**pat** - _string_ - the pattern to split on

## DESCRIPTION

**split** separates a string into a table of strings.  The strings are separated at each
occurrence of the supplied pattern. The pattern may be any pattern as described in the lua docs.
Each match of the pattern is consumed and not returned.

## RETURN VALUE

**result** - _table_ - a table of strings on success, or an empty table on error

## EXAMPLE
```
split("/a/long/path/name/to/a/file.txt", "/") 
```
would return a table like
```
{"a", "long", "path", "name", "to", "a", "file.txt"}
```
## REFERENCE

http://lua-users.org/wiki/SplitJoin
