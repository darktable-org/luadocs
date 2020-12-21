---
title: darktable.guides
id: darktable.guides
weight: 120
draft: false
author: "people"
---

`table`

Guide lines to overlay over an image in crop and rotate.
All guides are clipped to the drawing area.

# darktable.guides.register_guide

```
function(
  name : string,
  draw_callback : function,
  [gui_callback : function]
)
```

Register a new guide.

* **name** - _string_ - The name of the guide to show in the GUI.
* **draw_callback** - _function_ - The function to call to draw the guide lines.
* **\[gui_callback\]** - _function_ - A function returning a widget to show when the guide is selected. It takes no arguments.

draw_callback -

```
function(
  cr : types.dt_lua_cairo_t,
  x : float,
  y : float,
  width : float,
  height : float,
  zoom_scale : float
)
```

The function to call to draw the guide lines. The drawn lines will be stroked by darktable.
**THIS IS RUNNING IN THE GUI THREAD AND HAS TO BE FAST!**

* **cr** - _[types.dt_lua_cairo_t](../../types/dt_lua_cairo_t)_ - The cairo object used for drawing.
* **x** - _float_ - The x coordinate of the top left corner of the drawing area.
* **y** - _float_ - The y coordinate of the top left corner of the drawing area.
* **width** - _float_ - The width of the drawing area.
* **height** - _float_ - The height of the drawing area.
* **zoom_scale** - _float_ -The current zoom_scale. Only needed when setting the line thickness.

