---
title: check_if_bin_exists
id: check_if_bin_exists
weight: 20
draft: false
author: "people"
---

## NAME

check_if_bin_exists

## SYNOPSIS

check if an executable exists

## USAGE
```
local df = require "lib/dtutils.file"
local result = df.check_if_bin_exists(bin)
```
**bin** - _string_ - the binary to check for

## DESCRIPTION

**check_if_bin_exists** checks to see if the specified binary exists.
**check_if_bin_exists** first checks to see if a preference for the binary has been
registered and uses that if found.  The presence of the file is verified, then 
quoted and returned.  If no preference is specified and the operating system is
linux then the which command is used to check for a binary in the path.  If found
that path is returned.  If no binary is found, false is returned.

## RETURN VALUE

**result** - _string_ - the sanitized path of the binary, false if not found
