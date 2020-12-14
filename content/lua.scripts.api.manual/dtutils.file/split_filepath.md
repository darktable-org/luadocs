---
title: split_filepath
id: split_filepath
weight: 190
draft: false
author: "people"
---

## NAME

split_filepath

## SYNOPSIS

split a filepath into parts

## USAGE
```
local df = require "lib/dtutils.file"
local result = df.split_filepath(filepath)
```
**filepath** - _string_ - path and filename

## DESCRIPTION

**split_filepath** splits a filepath into the path, filename, basename and filetype and puts
that in a table

## RETURN VALUE

**result** - _table_ - a table containing the path, filename, basename, and filetype
