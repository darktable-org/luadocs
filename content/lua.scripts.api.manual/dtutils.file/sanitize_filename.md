---
title: sanitize_filename
id: sanitize_filename
weight: 170
draft: false
author: "people"
---

## NAME

sanitize_filename

## SYNOPSIS

make a filename safe to pass as an argument

## USAGE
```
local df = require "lib/dtutils.file"
local sanitized_filename = df.sanitize_filename(filename)
```
**filename** - _string_ - a filepath and filename

## DESCRIPTION

**sanitize_filename** places quotes around the filename in an
operating system specific manner.  The result is safe to pass as 
an argument to the operating system.

## RETURN VALUE

**sanitized_filename** - _string_ - quoted filename
