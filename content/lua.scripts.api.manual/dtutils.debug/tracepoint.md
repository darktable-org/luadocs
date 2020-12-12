---
title: tracepoint
id: tracepoint
weight: 50
draft: false
author: "people"
---

## NAME

tracepoint

## SYNOPSIS

print out a tracepoint and dump the arguments

## USAGE
```
local dd = require "lib/dtutils.debug"
local result = dd.tracepoint(name, ...)
```
**name** - _string_ - the name of the tracepoint to print out  
**...** - _arguments_ - variables to dump the contents of

## DESCRIPTION

**tracepoint** prints its name and dumps its parameters using
**darktable.debug**.

## RETURN VALUE

**result** - _..._ - the supplied argument list
