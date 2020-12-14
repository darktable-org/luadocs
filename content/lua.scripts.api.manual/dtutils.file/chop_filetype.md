---
title: chop_filetype
id: chop_filetype
weight: 40
draft: false
author: "people"
---

## NAME

chop_filetype

## SYNOPSIS

remove a filetype from a filename

## USAGE
```
local df = require "lib/dtutils.file"
local result = df.chop_filetype(path)
```
**path** - _string_ - a filename with or without a path

## DESCRIPTION

**chop_filetype** removes the filetype from the filename.

## RETURN VALUE

**result** - _string_ - the path and filename without the filetype
