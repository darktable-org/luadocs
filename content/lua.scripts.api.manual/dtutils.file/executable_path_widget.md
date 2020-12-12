---
title: executable_path_widget
id: executable_path_widget
weight: 60
draft: false
author: "people"
---

## NAME

executable_path_widget

## SYNOPSIS

create a widget to get executable path preferences

## USAGE
```
local df = require "lib/dtutils.file"
local widget = df.executable_path_widget(executables)
```
**executables** - _table_ - a table of strings that are executable names

## DESCRIPTION

**executable_path_widget** takes a table of executable names
and builds a set of file selector widgets to get the path to the executable. 
The resulting widgets are wrapped in a box widget and returned.

## RETURN VALUE

**widget** - _widget_ - a widget containing a file selector widget for
each executable.
