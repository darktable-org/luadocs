---
title: set_executable_path_preference
id: set_executable_path_preference
weight: 180
draft: false
author: "people"
---

## NAME

set_executable_path_preference

## SYNOPSIS

set a preference for the path to an executable

## USAGE
```
local df = require "lib/dtutils.file"
df.set_executable_path_preference(executable, path)
```
**executable** - _string_ - the name of the executable to set the path for  
**path** - _string_ - the path to the binary

## DESCRIPTION

**set_executable_path_preference** takes an executable name and path to the
executable and registers the preference for later use.
