---
title: check_min_api_version
id: check_min_api_version
weight: 20
draft: false
author: "people"
---

## NAME

check_min_api_version

## SYNOPSIS

check the minimum required application programming interface (API) version against the current API version

## USAGE
```
local du = require "lib/dtutils"
local result = du.check_min_api_version(min_api, script_name)
```
**min_api** - _string_ - the API version that the application was written for (example: "5.0.0")  
**script_name** - _string_ - the name of the script

## DESCRIPTION

**check_min_api_version** compares the minimum API required for the application to
run against the current API version. The minimum API version is typically the API version that 
was current when the application was created. If the minimum API version is not met, then an 
error message is printed saying the script_name failed to load, then an error is thrown causing the
program to stop executing. 

This function is intended to replace **darktable.configuration.check_version()**. The application code
won't have to be updated each time the API changes because this only checks the minimum version required.

## RETURN VALUE

**result** - _boolean_ - true if the minimum API version is available, false if not.

## LIMITATIONS

When using the default handler on a script being executed from the luarc file, the error thrown
will stop the luarc file from executing any remaining statements. This limitation does not apply to script_manger.

## EXAMPLE
```
check_min_api_version("5.0.0") 
```
does nothing if the API is greater than or equal to 5.0.0 otherwise an
error message is printed and an error is thrown stopping execution of the script.
