---
title: check_os
id: check_os
weight: 30
draft: false
author: "people"
---

## NAME

check_os

## SYNOPSIS

check that the operating system is supported

## USAGE
```
local du = require "lib/dtutils"
local result = du.check_os(operating_systems)
```
**operating_systems** - _table_ - a table of operating system names such as {"windows","linux","macos","unix"}

## DESCRIPTION

**check_os** checks a supplied table of operating systems against the operating system the
script is running on and returns true if the OS is in the list, otherwise false

## RETURN VALUE

**result** - _boolean_ - true if the operating system is supported, false if not.

## EXAMPLE
```
local du = require "lib/dtutils"
if du.check_os({"windows"}) then
  -- run the script
else
  dt.print("Script <script name> only runs on windows")
  return
end
```