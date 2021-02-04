---
title: darktable.gui.views.lighttable
id: lighttable
weight: 30
draft: false
author: "people"
---

The lighttable view

Attributes:
* [has_tostring](../../../Attributes#has_tostring)
* [parent](../../../Attributes#parent) : [types.dt_lua_view_t](../../../types/dt_lua_view_t)

## darktable.gui.views.lighttable.is_image_visible

```
function(
  image : types.dt_lua_image_t
) : types.dt_lua_image_t
```

Check if the image is visible in lighttable view. The lighttable must be in file manager or
zoomable mode.

* **image** - _[types.dt_lua_image_t](../../../types/dt_lua_image_t)_ - The image to be checked.
* **return** - _boolean_ - True if the image is displayed. False if the image is partially displayed or not displayed.

## darktable.gui.views.lighttable.set_image_visible

```
function(
  image : types.dt_lua_image_t
) : types.dt_lua_image_t
```

Set the image visible in lighttable view. The lighttable must be in file manager or zoomable
mode.

* **image** - _[types.dt_lua_image_t](../../../types/dt_lua_image_t)_ - The image to set visible.
* **return** - _int_ - An error is returned if no image is specified.
