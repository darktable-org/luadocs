---
title: check_max_api_version
id: check_max_api_version
weight: 15
draft: false
author: "people"
---

## NAME

check_max_api_version

## SYNOPSIS

check the maximum required application programming interface (API) version against the current API version

## USAGE
```
local du = require "lib/dtutils"
local result = du.check_max_api_version(max_api, script_name)
```
**max_api** - _string_ - the maximum API version that the application was written for (example: "5.0.0")  
**script_name** - _string_ - the name of the script

## DESCRIPTION

**check_max_api_version** compares the maximum API required for the application to
run against the current API version. This function is used when a part of the Lua API that
the script relies on is removed.  If the maximum API version is not met, then an 
error message is printed saying the script_name failed to load, then an error is thrown causing the
program to stop executing. 

## RETURN VALUE

**result** - _boolean_ - true if the maximum API version is available, false if not.

## LIMITATIONS

When using the default handler on a script being executed from the luarc file, the error thrown
will stop the luarc file from executing any remaining statements. This limitation does not apply to script_manger.

## EXAMPLE
```
check_max_api_version("5.0.0") 
```
does nothing if the API is less than or equal to 5.0.0 otherwise an
error message is printed and an error is thrown stopping execution of the script.
