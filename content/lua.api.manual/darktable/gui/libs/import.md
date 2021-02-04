---
title: darktable.gui.libs.import
id: import
weight: 180
draft: false
author: "people"
---

The buttons to start importing images

Attributes:
* [has_tostring](../../../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../../types/dt_lua_lib_t)

## darktable.gui.libs.import.register_widget

```
function(
  widget : types.lua_widget
)
```

Add a widget in the option expander of the import dialog

* **widget** - _[types.lua_widget](../../../types/lua_widget)_ - The widget to add to the dialog. The reset callback of the widget will be called whenever the dialog is opened.

