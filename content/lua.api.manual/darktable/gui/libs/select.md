---
title: darktable.gui.libs.select
id: select
weight: 320
draft: false
author: "people"
---

The buttons that allow to quickly change the selection

Attributes:
* [has_tostring](../../../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../../types/dt_lua_lib_t)

## darktable.gui.libs.select.register_selection

```
function(
  label : string,
  callback : function,
  [tooltip : string]
)
```

Add a new button and call a callback when it is clicked

* **label** - _string_ - The label to display on the button
* **callback** - _function_ - The function to call when the button is pressed
* **\[tooltip\]** - _string_ - The tooltip to use on the new button

callback -

```
function(
  event : string,
  images : table oftypes.dt_lua_image_t
) : table oftypes.dt_lua_image_t
```

The function to call when the button is pressed

* **event** - _string_ - The name of the button that was pressed
* **images** - _table of [types.dt_lua_image_t](../../../types/dt_lua_image_t)_ - The images in the current collection. This is the same content asdarktable.collection
* **return** - _table of [types.dt_lua_image_t](../../../types/dt_lua_image_t)_ - The images to set the selection to
