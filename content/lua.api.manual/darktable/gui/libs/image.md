---
title: darktable.gui.libs.image
id: image
weight: 170
draft: false
author: "people"
---

The UI element that manipulates the current images

Attributes:
* [has_tostring](../../../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../../types/dt_lua_lib_t)

## darktable.gui.libs.image.register_action

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
)
```

The function to call when the button is pressed

* **event** - _string_ - The name of the button that was pressed
* **images** - _table of [types.dt_lua_image_t](../../../types/dt_lua_image_t)_ - The images to act on when the button was clicked
