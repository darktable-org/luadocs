---
title: attributes
id: attributes
weight: 50
draft: false
author: "people"
---

This section documents various attributes used throughout the documentation.

# write

This object is a variable that can be written to.

# has_tostring

This object has a specific reimplementation of the "tostring" method that allows pretty-printing it.

# implicit_yield

This call will release the Lua lock while executing, thus allowing other Lua callbacks to run.

# parent

This object inherits some methods from another object. You can call the methods from the parent on the child object

