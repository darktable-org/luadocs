---
title: get_path
id: get_path
weight: 140
draft: false
author: "people"
---

## NAME

get_path

## SYNOPSIS

get the path from a file path

## USAGE
```
local df = require "lib/dtutils.file"
local result = df.get_path(filepath)
```
**filepath** - _string_ - path and filename

## DESCRIPTION

**get_path** strips the filename and filetype from a path and returns the path

## RETURN VALUE

**result** - _string_ - the path
