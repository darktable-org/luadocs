---
title: get_filename
id: get_filename
weight: 120
draft: false
author: "people"
---

## NAME

get_filename

## SYNOPSIS

get the filename and extension from a file path

## USAGE
```
local df = require "lib/dtutils.file"
local result = df.get_filename(filepath)
```
**filepath** - _string_ - path and filename

## DESCRIPTION

**get_filename** strips the path from a filepath and returns the filename

## RETURN VALUE

**result** - _string_ - the file name and type
