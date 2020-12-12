---
title: rmdir
id: rmdir
weight: 160
draft: false
author: "people"
---

## NAME

rmdir

## SYNOPSIS

recursively remove a directory

## USAGE
```
local df = require "lib/dtutils.file"
df.rmdir(path)
```
**path** - _string_ - a directory path

## DESCRIPTION

**rmdir** allows directories to be removed recursively.

## RETURN VALUE

**path** - _string_ - a directory path
