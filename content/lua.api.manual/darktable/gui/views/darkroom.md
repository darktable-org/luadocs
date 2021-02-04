---
title: darktable.gui.views.darkroom
id: darkroom
weight: 20
draft: false
author: "people"
---
The darkroom view

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_view_t](../../types/dt_lua_view_t)

## darktable.gui.views.darkroom.display_image

```
function(
  [image : types.dt_lua_image_t]
) : types.dt_lua_image_t
```

Display an image in darkroom view.
* **\[image\] - _[types.dt_lua_image_t](../../../types/dt_lua_image_t)_ - The image to be displayed. If the image is not given, nothing will be changed.
* **return** - _[types.dt_lua_image_t](../../../types/dt_lua_image_t)_ - The image currently displayed.
