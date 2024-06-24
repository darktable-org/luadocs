---
title: build_substitute_list
id: build_substitute_list
weight: 90
draft: false
author: "people"
---

## NAME

build_substitute_list

## SYNOPSIS

build a list of variable substitutions

## USAGE
```
local ds = require "lib/dtutils.string"
local result = ds.build_substitute_list(image, sequence, variable_string, [username], [pic_folder], [home], [desktop])
```
* **image** - _[dt_lua_image_t](../../lua.api.manual/types/dt_lua_image_t.md)_ - the image being processed
* **sequence** - _integer_ - the sequence number of the image being processed (exported)
* **variable_string** - _string_ - the substitution variable string
* **\[username\]** - _string_ - optional - user name.  Will be determined if not supplied
* **\[pic_folder\]** - _string_ - optional - pictures folder name.  Will be determined if not supplied
* **\[home\]** - _string_ - optional - home directory.  Will be determined if not supplied
* **\[desktop\]** - _string_ - optional - desktop directory.  Will be determined if not supplied

## DESCRIPTION

**build_substitute_list** populates variables with values from the arguments
and determined from the system and darktable.

## RETURN VALUE



## LIMITIATIONS

If the value for a variable can not be determined, or is not supported,
then an empty string is used for the value

## SEE ALSO

[darktable variables](https://docs.darktable.org/usermanual/4.6/en/special-topics/variables/)