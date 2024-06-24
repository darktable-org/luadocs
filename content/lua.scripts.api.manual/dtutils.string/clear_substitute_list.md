---
title: clear_substitute_list
id: clear_substitute_list
weight: 80
draft: false
author: "people"
---

## NAME

clear_substitute_list

## SYNOPSIS

Clear the computed list of variable substitution values.

## USAGE
```
local ds = require "lib/dtutils.string"
local result = ds.clear_substitute_list()
```
## DESCRIPTION

**clear_substitute_list** resets the list of variable replacement values in 
preparation for running [build_substitute_list](build_substitute_list.md)

## RETURN VALUE


