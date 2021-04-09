---
title: test_file
id: test_file
weight: 200
draft: false
author: "people"
---

## NAME

test_file

## SYNOPSIS

test a file to see what it is

## USAGE
```
local df = require "lib/dtutils.file"
local result = df.test_file(path, test)
```
**path** - _string_ - path and filename 
**test** - _char_ - one of d, e, f, x where
* d - directory
* e - exists
* f - file 
* x - executable

## DESCRIPTION

**test_file** checks a specified path to see if it meets the specified test

## RETURN VALUE

**result** - _boolean_ - true if the path satisfies the test, false if not
