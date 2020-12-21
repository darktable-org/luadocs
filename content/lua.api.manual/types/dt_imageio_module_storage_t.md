---
title: dt_imageio_module_storage_t
id: dt_imageio_module_storage_t
weight: 180
draft: false
author: "people"
---

`dt_type`

A virtual type representing all storage types.

# dt_imageio_module_storage_t.plugin_name

`string`

A unique name for the plugin.

Attributes:

* [write](../attributes#write)

# dt_imageio_module_storage_t.name

`string`

A human readable name for the plugin.

Attributes:

* [write](../attributes#write)

# dt_imageio_module_storage_t.width

`number`

The currently selected width for the plugin.

Attributes:

* [write](../attributes#write)

# dt_imageio_module_storage_t.height

`number`

The currently selected height for the plugin.

Attributes:

* [write](../attributes#write)

# dt_imageio_module_storage_t.recommended_width

`number`
The recommended width for the plugin.

Attributes:

* [write](../attributes#write)

# dt_imageio_module_storage_t.recommended_height

`number`

The recommended height for the plugin.

Attributes:

* [write](../attributes#write)

# dt_imageio_module_storage_t.supports_format
```
format : types.dt_imageio_module_format_t
) : boolean
```

Checks if a format is supported by this storage.

* **self** - _[types.dt_imageio_module_storage_t](../types/dt_imageio_module_storage_t)_ - The storage type to check against.
* **format** - _[types.dt_imageio_module_format_t](../types/dt_imageio_module_format_t)_ - The format type to check.
* **return** - _boolean_ - True if the format is supported by the storage.

