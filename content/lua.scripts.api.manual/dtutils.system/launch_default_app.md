---
title: launch_default_app
id: launch_default_app
weight: 30
draft: false
author: "people"
---

## NAME

launch_default_app

## SYNOPSIS

open file in default application

## USAGE
```
local dsys = require "lib/dtutils.file"
result = dsys.launch_default_app(path)
```
**path** - _string_ - a file path

## DESCRIPTION

**launch_default_app** allows opening a file in the application that is assigned as default 
for that filetype in the users's system

## RETURN VALUE

**result** - _number_ - the return value signalling success or failure.
