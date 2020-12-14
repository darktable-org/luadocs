---
title: get_executable_path_preference
id: get_executable_path_preference
weight: 110
draft: false
author: "people"
---

## NAME

get_executable_path_preference

## SYNOPSIS

return the path to an executable from a preference

## USAGE
```
local df = require "lib/dtutils.file"
local result = df.get_executable_path_preference(executable)
```
**executable** - _string_ - the name of the executable to get the path for

## DESCRIPTION

**get_executable_path_preference** returns the path preference to
the requested executable.

## RETURN VALUE

**result** - _string_ - path to the executable

## LIMITATIONS

executable should be the basename of the executable without extensions
