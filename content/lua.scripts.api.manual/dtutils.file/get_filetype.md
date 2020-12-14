---
title: get_filetype
id: get_filetype
weight: 130
draft: false
author: "people"
---

## NAME

get_filetype

## SYNOPSIS

get the filetype from a filename

## USAGE
```
local df = require "lib/dtutils.file"
local result = df.get_filetype(filepath)
```
**filepath** - _string_ - path and filename

## DESCRIPTION

**get_filetype** returns the filetype from the supplied filepath

## RETURN VALUE

**result** - _string_ - the filetype
