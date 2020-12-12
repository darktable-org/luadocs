---
title: file_move
id: file_move
weight: 80
draft: false
author: "people"
---

## NAME

file_move

## SYNOPSIS

move a file from one directory to another

## USAGE
```
local df = require "lib/dtutils.file"
local result = df.file_move(fromFile, toFile)
```
**fromFile** - _string_ - name of the original file  
**toFile** - _string_ - the new file location and name

## DESCRIPTION

Move a file from one place to another.  Try a succession of methods from
builtin to operating system to a pure lua solution.

## RETURN VALUE

**result** - _boolean_ - nil on error, some value on success
