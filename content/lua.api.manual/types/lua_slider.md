---
title: lua_slider
id: lua_slider
weight: 640
draft: false
author: "people"
---

`dt_type`

A slider that can be set by the user

Attributes:

* [has_tostring](../attributes#has_tostring)
* [parent](../attributes#parent) : [types.lua_widget](../types/lua_widget)

2.63.1. types.lua_slider.\_\_call
see [types.lua_widget.As a function](../types/lua_widget#lua_widgetas-a-function)

2.63.2. types.lua_slider.extra registration parameters
This widget has no extra registration parameters

2.63.3. types.lua_slider.soft_min

`number`

The soft minimum value for the slider, the slider can't go beyond this point

Attributes:

* [write](../attributes#write)

2.63.4. types.lua_slider.soft_max

`number`

The soft maximum value for the slider, the slider can't go beyond this point


Attributes:

* [write](../attributes#write)

2.63.5. types.lua_slider.hard_min

`number`

The hard minimum value for the slider, the user can't manually enter a value beyond this
point
Attributes:


* [write](../attributes#write)

2.63.6. types.lua_slider.hard_max

`number`

The hard maximum value for the slider, the user can't manually enter a value beyond this
point

Attributes:

* [write](../attributes#write)

2.63.7. types.lua_slider.step

`number`

The step width of the slider

Attributes:

* [write](../attributes#write)

2.63.8. types.lua_slider.digits

`integer`

The number of decimal digits shown on the slider

Attributes:

* [write](../attributes#write)

2.63.9. types.lua_slider.value

`number`

The current value of the slider

Attributes:

* [write](../attributes#write)

2.63.10. types.lua_slider.label

`string`

The label next to the slider

Attributes:

* [write](../attributes#write)
