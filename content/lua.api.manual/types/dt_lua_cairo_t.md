---
title: dt_lua_cairo_t
id: dt_lua_cairo_t
weight: 340
draft: false
author: "people"
---

`dt_type`

A wrapper around a cairo drawing context.
You probably shouldn't use this after the callback that got it passed returned.
For more details of the member functions have a look at the cairo documentation for
the [drawing context](http://www.cairographics.org/manual/cairo-cairo-t.html), [transformations](http://www.cairographics.org/manual/cairo-Transformations.html) and [paths](http://www.cairographics.org/manual/cairo-Paths.html).

# dt_lua_cairo_t.save
```
self:function(
)
```

Save the state of the drawing context.

* **self** - _[types.dt_lua_cairo_t](../types/dt_lua_cairo_t)_ - The context to modify.

# types.dt_lua_cairo_t.restore
```
self:function(
)
```

Restore a previously saved state.

* **self** - _[types.dt_lua_cairo_t](../types/dt_lua_cairo_t)_ - The context to modify.

# dt_lua_cairo_t.move_to
```
self:function(
  x : float,
  y : float
)
```

Begin a new sub-path.

* **self** - _[types.dt_lua_cairo_t](../types/dt_lua_cairo_t)_ - The context to modify
* **x** - _float_ - The x coordinate of the new position.
* **y** - _float_ - The y coordinate of the new position.

# dt_lua_cairo_t.line_to
```
self:function(
  x : float,
  y : float
)
```

Add a line to the path.

* **self** - _[types.dt_lua_cairo_t](../types/dt_lua_cairo_t)_ - The context to modify.
* **x** - _float_ - The x coordinate of the end of the new line.
* **y** - _float_ - The y coordinate of the end of the new line.

# types.dt_lua_cairo_t.rectangle
```
self:function(
  x : float,
  y : float,
  width : float,
  height : float
)
```

Add a closed sub-path rectangle.

* **self** - _[types.dt_lua_cairo_t](../types/dt_lua_cairo_t)_ - The context to modify.
* **x** - _float_ - The x coordinate of the top left corner of the rectangle.
* **y** - _float_ - The y coordinate of the top left corner of the rectangle.
* **width** - _float_ - The width of the rectangle.
* **height** - _float_ - The height of the rectangle.

# dt_lua_cairo_t.arc
```
self:function(
  x : float,
  y : float,
  radius : float,
  angle1 : float,
  angle2 : float
)
```

Add a circular arc.

* **self** - _[types.dt_lua_cairo_t](../types/dt_lua_cairo_t)_ - The context to modify.
* **x** - _float_ - The x position of the center of the arc.
* **y** - _float_ - The y position of the center of the arc.
* **radius** - _float_ - The radius of the arc.
* **angle1** - _float_ - The start angle, in radians.
* **angle2** - _float_ - The end angle, in radians.

# dt_lua_cairo_t.arc_negative
```
self:function(
  x : float,
  y : float,
  radius : float,
  angle1 : float,
angle2 : float
)
```

Add a circular arc. It only differs in the direction from types.dt_lua_cairo_t.arc.

* **self** - _[types.dt_lua_cairo_t](../types/dt_lua_cairo_t)_ - The context to modify.
* **x** - _float_ - The x position of the center of the arc.
* **y** - _float_ - The y position of the center of the arc.
* **radius** - _float_ - The radius of the arc.
* **angle1** - _float_ - The start angle, in radians.
* **angle2** - _float_ - The end angle, in radians.

# dt_lua_cairo_t.rotate
```
self:function(
  angle : float
)
```

Add a rotation to the transformation matrix.

* **self** - _[types.dt_lua_cairo_t](../types/dt_lua_cairo_t)_ - The context to modify.
* **angle** - _float_ - The angle (in radians) by which the user-space axes will be rotated.

# dt_lua_cairo_t.scale
```
self:function(
  x : float,
  y : float
)
```

Add a scaling to the transformation matrix.

self** - _[types.dt_lua_cairo_t](../types/dt_lua_cairo_t)_ - The context to modify.
* **x** - _float_ - The scale factor for the x dimension.
* **y** - _float_ - The scale factor for the y dimension.

# dt_lua_cairo_t.translate
```
self:function(
  x : float,
  y : float
)
```

Add a translation to the transformation matrix.

* **self** - _[types.dt_lua_cairo_t](../types/dt_lua_cairo_t)_ - The context to modify.
* **x** - _float_ - Amount to translate in the x direction
* **y** - _float_ - Amount to translate in the y direction

# dt_lua_cairo_t.new_sub_path
```
self:function(
)
```

Begin a new sub-path.

* **self** - _[types.dt_lua_cairo_t](../types/dt_lua_cairo_t)_ - The context to modify.

# dt_lua_cairo_t.draw_line
```
self:function(
  x_start : float,
  y_start : float,
  x_end : float,
  y_end : float
)
```

Helper function to draw a line with a given start and end.

* **self** - _[types.dt_lua_cairo_t](../types/dt_lua_cairo_t)_ - The context to modify.
* **x_start** - _float_ - The x coordinate of the start of the new line.
* **y_start** - _float_ - The y coordinate of the start of the new line.
* **x_end** - _float_ - The x coordinate of the end of the new line.
* **y_end** - _float_ - The y coordinate of the end of the new line.

