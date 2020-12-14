---
title: dprint
id: dprint
weight: 20
draft: false
author: "people"
---

## NAME

dprint

## SYNOPSIS

pass a variable to darktable.debug.dump and print the results to stdout

## USAGE
```
local dd = require "lib/dtutils.debug"
dd.dprint(var)
```
**var** - _variable_ - any variable that you want to see the contents of

## DESCRIPTION

**dprint** is a wrapper around **darktable.debug.dump**, will directly print to stdout,
same calling convention
