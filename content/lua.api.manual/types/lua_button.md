---
title: lua_button
id: lua_button
weight: 500
draft: false
author: "people"
---

`dt_type`

A clickable button

Attributes:

* [has_tostring](../attributes#has_tostring)
* [parent](../attributes#parent) : [types.lua_widget](../types/lua_widget)

# lua_button.\_\_call
see [types.lua_widget.As a function](../types/lua_widget#lua_widgetas-a-function)

# lua_button.extra registration parameters
This widget has no extra registration parameters

# lua_button.label

`string`

The label displayed on the button

Attributes:

* [write](../attributes#write)

# lua_button.halign

[types.dt_lua_align_t](../types/dt_lua_align_t)

The horizontal alignment of the button label

Attributes:

* [write](../attributes#write)

# lua_button.ellipsize

[types.dt_lua_ellipsize_mode_t](../types/dt_lua_ellipsize_mode_t)

The ellipsize mode of the button label

Attributes:

* [write](../attributes#write)

# lua_button.image

`image`

The image displayed on the button instead of a label

Attributes:

* [write](../attributes#write)

# lua_button.image_align

[types.dt_lua_align_t](../types/dt_lua_align_t)

The horizontal alignment of the button image

Attributes:

* [write](../attributes#write)

# lua_button.clicked_callback
```
function(
  widget : types.lua_widget
)
```
A function to call on button click

* **widget** - _[types.lua_widget](../types/lua_widget)_ - The widget that triggered the callback

Attributes:

* [write](../attributes#write)

