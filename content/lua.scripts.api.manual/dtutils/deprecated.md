---
title: deprecated
id: deprecated
weight: 32
draft: false
author: "people"
---

## NAME

deprecated

## SYNOPSIS

warn that a script is deprecated

## USAGE
```
local du = require "lib/dtutils"
du.deprecated(script_name, deprecation_time)
```
**script_name** - _string_ - the name of the script, i.e. "contrib/clear_GPS"  
**deprecation_time** - _string_ - when the script will be removed, i.e. "darktable release 4.0"

## DESCRIPTION

**deprecated** gives users a warning that a script is outdated or no longer useful and will be
removed at the specified time

