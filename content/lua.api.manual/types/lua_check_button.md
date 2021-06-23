---
title: lua_check_button
id: lua_check_button
weight: 510
draft: false
author: "people"
---

`dt_type`

A checkable button with a label next to it
Attributes:

* [has_tostring](../attributes#has_tostring)
* [parent](../attributes#parent) : [types.lua_widget](../types/lua_widget)

# lua_check_button.\_\_call
see [types.lua_widget.As a function](../types/lua_widget#lua_widgetas-a-function)

# lua_check_button.extra registration parameters

This widget has no extra registration parameters

# lua_check_button.label

`string`

The label displayed next to the button

Attributes:

* [write](../attributes#write)

# lua_check_button.value

`boolean`

If the widget is checked or not

Attributes:

* [write](../attributes#write)

# lua_check_button.clicked_callback
```
function(
  widget : types.lua_widget
)
```

A function to call on button click

* **widget** - _[types.lua_widget](../types/lua_widget)_ - The widget that triggered the callback

Attributes:

* [write](../attributes#write)

