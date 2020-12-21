---
title: darktable.styles
id: darktable.styles
weight: 160
draft: false
author: "people"
---

This pseudo table allows you to access and manipulate styles.

# darktable.styles.#

[types.dt_style_t](../../types/dt_style_t)

Each existing style has a numeric index; you can iterate them using ipairs.

# darktable.styles.create

```
function(
  image : types.dt_lua_image_t,
  name : string,
  description : string
) : types.dt_style_t
```

Create a new style based on an image.

* **image** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The image to create the style from.
* **name** - _string_ - The name to give to the new style.
* **description** - _string_ - The description of the new style.
* **return** - _[types.dt_style_t](../../types/dt_style_t)_ - The new style object.

# darktable.styles.delete

```
function(
  style : types.dt_style_t
)
```

Deletes an existing style.

* **style** - _[types.dt_style_t](types.dt_style_t)_ - the style to delete

# darktable.styles.duplicate

```
function(
  style : types.dt_style_t,
  name : string,
  description : string
) : types.dt_style_t
```

Create a new style based on an existing style.

* **style** - _[types.dt_style_t](../../types/dt_style_t)_ - The style to base the new style on.
* **name** - _string_ - The new style's name.
* **description** - _string_ - The new style's description.
* **return** - _[types.dt_style_t](../../types/dt_style_t)_ - The new style object.

# darktable.styles.apply

```
function(
  style : types.dt_style_t,
  image : types.dt_lua_image_t
)
```

Apply a style to an image. The order of parameters can be inverted.

* **style** - _[types.dt_style_t](../../types/dt_style_t)_ - The style to use.
* **image** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The image to apply the style to.

# darktable.styles.import

```
function(
  filename : string
)
```

Import a style from an external .dtstyle file

* **filename** - _string_ - The file to import

# darktable.styles.export

```
function(
  style : types.dt_style_t,
  directory : string,
  overwrite : boolean
)
```

Export a style to an external .dtstyle file

* **style** - _[types.dt_style_t](../../types/dt_style_t)_ - The style to export
* **directory** - _string_ - The directory to export to
* **overwrite** - _boolean_ - Is overwriting an existing file allowed
