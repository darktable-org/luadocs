---
title: substitute
id: substitute
weight: 110
draft: false
author: "people"
---

## NAME

substitute

## SYNOPSIS

perform all the variable substitution steps with one function call

## USAGE
```
local ds = require "lib/dtutils.string"
local result = ds.substitute(image, sequence, variable_string, [username], [pic_folder], [home], [desktop])
```
* **image** - _[dt_lua_image_t](../../lua.api.manual/types/dt_lua_image_t.md)_ - the image being processed
* **sequence** - _integer_ - the sequence number of the image being processed (exported)
* **variable_string** - _string_ - the substitution variable string
* **\[username\]** - _string_ - optional - user name.  Will be determined if not supplied
* **\[pic_folder\]** - _string_ - optional - pictures folder name.  Will be determined if not supplied
* **\[home\]** - _string_ - optional - home directory.  Will be determined if not supplied
* **\[desktop\]** - _string_ - optional - desktop directory.  Will be determined if not supplied

## DESCRIPTION

**substitute** initializes the substitution list by calling [clear_substitute_list](clear_substitute_list.md),
    then builds the substitutions by calling [build_substitute_list](build_substitute_list.md) and finally does the 
    substitution by calling [substitute_list](substitute_list.md), then returns the result string.

## RETURN VALUE

**result** - _string_ - the input string with values substituted for the variables

## SEE ALSO

[darktable variables](https://docs.darktable.org/usermanual/4.6/en/special-topics/variables/)
