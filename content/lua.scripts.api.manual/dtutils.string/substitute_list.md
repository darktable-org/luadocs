---
title: substitute_list
id: substitute_list
weight: 100
draft: false
author: "people"
---

## NAME

substitute_list

## SYNOPSIS

replace variables in a string with their computed values

## USAGE
```
local ds = require "lib/dtutils.string"
local result = ds.substitute_list(str)
```
* **str** - _string_ - the string containing the variables to be substituted for

## DESCRIPTION

**substitute_list** replaces the variables in the supplied string with
values computed in [build_substitute_list](build_substitute_list.md).

## RETURN VALUE

**result** - _string_ - the input string with values substituted for the variables

## SEE ALSO

[darktable variables](https://docs.darktable.org/usermanual/4.6/en/special-topics/variables/)