---
title: dt_lua_backgroundjob_t
id: dt_lua_backgroundjob_t
weight: 330
draft: false
author: "people"
---

`dt_type`

A lua-managed entry in the backgroundjob lib

# dt_lua_backgroundjob_t.percent

`number`

The value of the progress bar, between 0 and 1. will return nil if there is no progress bar,
will raise an error if read or written on an invalid job

Attributes:

* [write](../attributes#write)

# dt_lua_backgroundjob_t.valid

`boolean`

True if the job is displayed, set it to false to destroy the entry
An invalid job cannot be made valid again

Attributes:

* [write](../attributes#write)

