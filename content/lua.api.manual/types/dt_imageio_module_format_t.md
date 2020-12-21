---
title: dt_imageio_module_format_t
id: dt_imageio_module_format_t
weight: 40
draft: false
author: "people"
---

`dt_type`

A virtual type representing all format types.

# dt_imageio_module_format_t.plugin_name

`string`

A unique name for the plugin.

# dt_imageio_module_format_t.name

`string`

A human readable name for the plugin.

# dt_imageio_module_format_t.extension

`string`

The typical filename extension for that format.

# dt_imageio_module_format_t.mime

`string`

The mime type associated with the format.

# dt_imageio_module_format_t.max_width

`number`

The max width allowed for the format \(0 = unlimited\).

Attributes:

* [write](../attributes#write)

2.3.6. dt_imageio_module_format_t.max_height

`number`

The max height allowed for the format \(0 = unlimited\).

Attributes:

* [write](../attributes#write)

2.3.7. dt_imageio_module_format_t.write_image
```
self:function(
  image : types.dt_lua_image_t,
  filename : string,
  [allow_upscale : boolean]
) : boolean
```
Exports an image to a file. This is a blocking operation that will not return until the image
is exported.

* **self** - _[types.dt_imageio_module_format_t](../types/dt_imageio_module_format_t)_ - The format that will be used to export.
* **image** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image object to export.
* **filename** - _string_ - The filename to export to.
* **\[allow_upscale\]** - _boolean_ - Set to true to allow upscaling of the image.
* **return** - _boolean_ - Returns true on success.

Attributes:

* [implicit_yield](../attributes#implicit_yield)

