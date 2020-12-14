---
title: join
id: join
weight: 40
draft: false
author: "people"
---

## NAME

join

## SYNOPSIS

join a table of strings with a specified separator

## USAGE
```
local du = require "lib/dtutils"
local result = du.join(tabl, pat)
```
**tabl** - _table_ - a table of strings  
**pat** - _string_ - a separator

## DESCRIPTION

**join** assembles a table of strings into a string with the specified pattern 
in between each string

## RETURN VALUE

**result** - _string_ - the joined string on success, or an empty string on failure

## EXAMPLE
```
join({a, "long", "path", "name", "to", a, "file.txt"}, " ")
```
 would return the string
"a long path name to a file.txt"

## REFERENCE

http://lua-users.org/wiki/SplitJoin
