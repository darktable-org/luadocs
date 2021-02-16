---
title: darktable.gui.libs.select
id: select
weight: 320
draft: false
author: "people"
---

The buttons that allow quickly changing the selection

Attributes:
* [has_tostring](../../../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../../types/dt_lua_lib_t)

## darktable.gui.libs.select.register_selection

```
function(
  name : string
  label : string,
  callback : function,
  [tooltip : string]
)
```

Add a new button and call a callback when it is clicked

* **name** - _string_ - The name to use to refer to the select button **API 6.2.2**
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

## darktable.gui.libs.select.destroy_selection **API 6.2.2**

```
function(
  name : string
)
```

Remove a button created by darktable.gui.libs.select.register_selection.

* **name** - _string_ - The name of the selection button to destroy

## darktable.gui.libs.select.selection_set_sensitive **API 6.2.2**

```
function(
  name : string
  sensitive : boolean
)
```

Set the sensitivity of a  button created by darktable.gui.libs.select.register_selection.

* **name** - _string_ - The name of the selection button to change the sensitivty of
* **sensitive** - _boolean_ - True to set the button sensitive, false to set it insensitive

