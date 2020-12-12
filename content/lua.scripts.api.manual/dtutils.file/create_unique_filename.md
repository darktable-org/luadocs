---
title: create_unique_filename
id: create_unique_filename
weight: 50
draft: false
author: "people"
---

## NAME

create_unique_filename

## SYNOPSIS

create a unique filename from the supplied argument

## USAGE
```
local df = require "lib/dtutils.file"
local result = df.create_unique_filename(filepath)
```
**filepath** - _string_ - the path and filename requested

## DESCRIPTION

**create_unique_filename** takes a requested filepath and checks to see if
it exists.  If if doesn't then it's returned intact.  If it already exists, then a two
digit increment is added to the filename and it is tested again.  The increment keeps 
increasing until either a unique filename is found or there have been 100 attempts.

## RETURN VALUE

**result** - _string_ - the incremented filename

## LIMITATIONS

**create_unique_filename** will only attempt 100 increments.
