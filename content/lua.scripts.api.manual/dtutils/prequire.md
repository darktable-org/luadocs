---
title: prequire
id: prequire
weight: 50
draft: false
author: "people"
---
## NAME

prequire

## SYNOPSIS

a protected lua require

## USAGE
```
local du = require "lib/dtutils"
local status, lib = du.prequire(req_name)
```
**req_name** - _string_ - the filename of the lua code to load without the ".lua" filetype

## DESCRIPTION

**prequire** is a protected require that can survive an error in the code being loaded without
bringing down the calling routine.

## RETURN VALUE

**status** - _boolean_ - true on success
**lib** - if status is true, then the code, otherwise an error message

## EXAMPLE
```
local status, lib = prequire("lib/dtutils.file") 
```
which would load lib/dtutils/file.lua which 
would return a status of true and the reference to the library.
