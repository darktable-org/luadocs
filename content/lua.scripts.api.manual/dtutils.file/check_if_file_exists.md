---
title: check_if_file_exists
id: check_if_file_exists
weight: 30
draft: false
author: "people"
---

## NAME

check_if_file_exists

## SYNOPSIS

check if a file or path exist

## USAGE
```
local df = require "lib/dtutils.file"
local result = df.check_if_file_exists(filepath)
```
**filepath** - _string_ - a file or path to check

## DESCRIPTION

**check_if_file_exists** checks to see if a file or path exists.

## RETURN VALUE

**result** - _boolean_ - true if the file or path exists, false if it doesn't.
