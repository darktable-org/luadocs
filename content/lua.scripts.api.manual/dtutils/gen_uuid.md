---
title: gen_uuid
id: gen_uuid
weight: 37
draft: false
author: "people"
---

## NAME

gen_uuid

## SYNOPSIS

Generate a UUID string

## USAGE
```
local du = require "lib/dtutils"
local uuid = du.gen_uuid(case)
```
**case** - string - "upper" or "lower" for the respective case.  If no argument is supplied, lower case is returned by default.  

## DESCRIPTION

**gen_uuid** generates a UUID string.

## RETURN VALUE

**uuid** - _string_ - A UUID formatted string in upper or lower case.

