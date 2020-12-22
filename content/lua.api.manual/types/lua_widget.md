---
title: lua_widget
id: lua_widget
weight: 530
draft: false
author: "people"
---

`dt_type`

Common parent type for all lua-handled widgets

Attributes:

* [has_tostring](../Attributes#has_tostring)

# lua_widget.extra registration parameters

This widget has no extra registration parameters

# lua_widget.sensitive

`boolean`

Set if the widget is enabled/disabled

Attributes:

* [write](../Attributes#write)

# lua_widget.tooltip

`string or nil`

Tooltip to display for the widget

Attributes:

* [write](../Attributes#write)

# lua_widget.reset_callback

```
function(
  widget : types.lua_widget
)
```

A function to call when the widget needs to reset itself.
Note that some widgets have a default implementation that can be overridden, \(containers in particular will recursively reset their children\). If you replace that default implementation you need to reimplement that functionality or call the original function within your
callback.

Attributes:

* [write](../Attributes#write)

* **widget** - _[types.lua_widget](../types.lua_widget)_ - The widget that triggered the callback

# lua_widget.As a function

```
function(
  attributes : table
) : types.lua_widget
```

Using a lua widget as a function Allows to set multiple attributes of that widget at once.
This is mainly used to create UI elements in a more readable way.

For example:

```
local widget = dt.new_widget("button"){
  label ="my label",
  clicked_callback = function() print "hello world" end
}
```

* **attributes** - _table_ - A table of attributes => value to set
* **return** - _[types.lua_widget](../types.lua_widget)_ - The object called itself, to allow chaining

