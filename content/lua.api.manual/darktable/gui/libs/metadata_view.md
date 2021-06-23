---
title: darktable.gui.libs.metadata_view
id: metadata_view
weight: 250
draft: false
author: "people"
---

The widget displaying metadata about the current image

Attributes:
* [has_tostring](../../../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../../types/dt_lua_lib_t)

## darktable.gui.libs.metadata_view.register_info

```
function(
  name : string,
  callback : function
)
```

Register a field in the image information module with a callback function to update the field

* **name** - _string_ - The name displayed for the new information
* **callback** - _function_ - The function providing the info

callback -

```
function(
  image : types.dt_lua_image_t
) : string
```

* **image** - _[types.dt_lua_image_t](../../../types/dt_lua_image_t)_ - The image to analyze
* **return** - _string_ - The extra information to display

## darktable.gui.libs.metadata_view.destroy_info

```
function(
  name : string
)
```

Remove the named field from the image information module and it's associated callback

* **name** - _string_ - The name of the field, created by [darktable.gui.libs.metadata_view.register_info](#darktable.gui.libs.metadata_view.register_info), to remove

