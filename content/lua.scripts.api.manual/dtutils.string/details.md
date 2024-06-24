---
title: details
id: details
weight: 10
draft: false
author: "people"
---

# DTUTILS.STRING

## NAME

dtutils.string

## SYNOPSIS

a library of string utilities for use in darktable lua scripts

## USAGE
```
local ds = require "lib/dtutils.string"
```
## DESCRIPTION

This library contains string manipulation routines to aid in building
darktable lua scripts.

## RETURN VALUE

_**ds** - library_ - the darktable lua string library

## FUNCTIONS

* [escape_xml_characters](escape_xml_characters.md) - escape characters for xml documents

* [is_not_sanitized](is_not_sanitized.md) - check if a string has been sanitized

* [sanitize](sanitize.md) - surround a string in quotes making it safe to pass as an argument

* [sanitize_lua](sanitize_lua.md) - escape lua 'magic' characters from a pattern string

* [strip_accents](strip_accents.md) - strip accents from characters

* [urlencode](urlencode.md) - encode a string in a websafe manner

* [clear_substitute_list](clear_substitute_list.md) - clear the computed list of variable substitution values

* [build_substitute_list](build_substitute_list.md) - build a list of variable substitutions

* [substitute_list](substitute_list.md) - replace variables in a string with their computed values

* [substitute](substitute.md) - perform all the variable substitution steps with one function call

## LICENSE

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 3 of the License, or
(at your option) any later version.
This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.
You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

