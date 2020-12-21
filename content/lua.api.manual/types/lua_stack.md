---
title: lua_stack
id: lua_stack
weight: 630
draft: false
author: "people"
---

`dt_type`

A container that will only show one of its child at a time

Attributes:

* [has_tostring](../attributes#has_tostring)
* [parent](../attributes#parent) : [types.lua_widget](../types/lua_widget)

# lua_stack.\_\_call
see [types.lua_widget.As a function](../types/lua_widget#lua_widgetas-a-function)

# lua_stack.extra registration parameters
This widget has no extra registration parameters

# lua_stack.active

[types.lua_widget](../types/lua_widget) or nil

The currently selected child, can be nil if the container has no child, can be set to one of
the child widget or to an index in the child table

Attributes:

* [write](../attributes#write)

# lua_stack.h_size_fixed

`boolean`

True if horizontal size is fixed, false if stack can be resized horizontally.

Attributes:

* [write](../attributes#write)

# lua_stack.v_size_fixed

`boolean`

True if vertical size is fixed, false if stack can be resized vertically.

Attributes:

* [write](../attributes#write)

