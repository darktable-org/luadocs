---
title: filename_increment
id: filename_increment
weight: 90
draft: false
author: "people"
---

## NAME

filename_increment

## SYNOPSIS

add a two digit increment to a filename

## USAGE
```
local df = require "lib/dtutils.file"
local result = df.filename_increment(filepath)
```
**filepath** - _string_ - filename to increment

## DESCRIPTION

**filename_increment** solves the problem of filename conflict by adding an 
increment to the filename.  If the supplied filename has no increment then 
"01" is added to the basename.  If the filename already has an increment, then
1 is added to it and the filename returned.

## RETURN VALUE

**result** - _string_ - the incremented filename

## LIMITATIONS

The filename will be incremented to a maximum of 99.
