---
title: file_copy
id: file_copy
weight: 70
draft: false
author: "people"
---

## NAME

file_copy

## SYNOPSIS

copy a file to another name/location

## USAGE
```
local df = require "lib/dtutils.file"
local result = df.file_copy(fromFile, toFile)
```
**fromFile** - _string_ - name of file to copy from  
**toFile** - _string_ - name of file to copy to

## DESCRIPTION

copy a file using a succession of methods from operating system
to a pure lua solution

## RETURN VALUE

**result** - _boolean_ - nil on error, true on success
