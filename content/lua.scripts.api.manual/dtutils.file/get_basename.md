---
title: get_basename
id: get_basename
weight: 100
draft: false
author: "people"
---

## NAME

get_basename

## SYNOPSIS

get the filename without the path or extension

## USAGE
```
local df = require "lib/dtutils.file"
local result = df.get_basename(filepath)
```
**filepath** - _string_ - path and filename

## DESCRIPTION

**get_basename** returns the name of the file without the path or filetype.

## RETURN VALUE

**result** - _string_ - the basename of the file
