---
title: sanitize_lua
id: sanitize_lua
weight: 50
draft: false
author: "people"
---

## NAME

sanitize_lua

## SYNOPSIS

escape lua 'magic' characters from a pattern string

## USAGE
```
local ds = require "lib/dtutils.string"
local result = ds.sanitize_lua(str)
```
**str** - _string_ - the string that needs to be made safe

## DESCRIPTION

**sanitize_lua** escapes lua 'magic' characters so that
a string may  be used in lua string/patten matching.

## RETURN VALUE

**result** - _string_ - a lua pattern safe string
