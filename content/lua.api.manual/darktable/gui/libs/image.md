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
  name : string,
  label : string,
  callback : function,
  [tooltip : string]
)
```

Add a new button and call a callback when it is clicked

* **name** - _string_ - A unique name for the action that can be referenced later to destroy it
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

## darktable.gui.libs.image.destroy_action

```
function(
  name : string
)
```

Destroy an action created with register_action

* **name** - _string_ - The name of the action to destroy

## darktable.gui.libs.image.action_set_sensitive

```
function(
  name : string,
  sensitive : boolean
)
```

Set the sensitivity of a button created by darktable.gui.libs.image.register_action

* **name** - _string_ - The name of the action to destroy
* **sensitive** - _boolean_ - True to set the button sensitive, false to set it insensitive

