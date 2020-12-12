---
title: new_tracepoint
id: new-tracepoint
weight: 30
draft: false
author: "people"
---

## NAME

new_tracepoint

## SYNOPSIS

create a function returning a tracepoint

## USAGE
```
local dd = require "lib/dtutils.debug"
local result = dd.new_tracepoint(name, ...)
```
**name** - _string_ - the name of the tracepoint to print out  
**...** - _arguments_ - variables to dump the contents of

## DESCRIPTION

**new_tracepoint** returns a tracepoint function with the given name.
This is mainly used to debug callbacks.

## RETURN VALUE

**result** - _function_ - a function that returns the result of a tracepoint

## EXAMPLE
```
register_event(event, dd.new_tracepoint("hit callback"))
```
will print the following each time the callback is called
```
**** hit callback ****
<all the callback's parameters dumped>
```
