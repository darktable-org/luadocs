---
title: dt_lua_lib_t
id: dt_lua_lib_t
weight: 380
draft: false
author: "people"
---

`dt_type`

The type of a UI lib

# dt_lua_lib_t.id

`string`

A unit string identifying the lib

# dt_lua_lib_t.name

`string`

The translated title of the UI element

# dt_lua_lib_t.version

`number`

The version of the internal data of this lib

# dt_lua_lib_t.visible

`boolean`

Allow to make a lib module completely invisible to the user.
Note that if the module is invisible the user will have no way to restore it without lua

Attributes:

* [implicit_yield](../attributes#implicit_yield)
* [write](../attributes#write)

# dt_lua_lib_t.container

[types.dt_ui_container_t](../types/dt_ui_container_t)

The location of the lib in the darktable UI

# dt_lua_lib_t.expandable

`boolean`

True if the lib can be expanded/retracted

# dt_lua_lib_t.expanded

`boolean`

True if the lib is expanded

Attributes:

* [write](../attributes#write)

# dt_lua_lib_t.position

`number`

A value deciding the position of the lib within its container

# dt_lua_lib_t.views

`table`

A table of all the views that display this widget

# dt_lua_lib_t.reset
```
self:function(
)
```
A function to reset the lib to its default values
This function will do nothing if the lib is not visible or can't be reset

* **self** - _[types.dt_lua_lib_t](../types/dt_lua_lib_t)_ - The lib to reset

# dt_lua_lib_t.on_screen

`boolean`

True if the lib is currently visible on the screen

