---
title: darktable.register_storage
id: darktable.register_storage
weight: 50
draft: false
author: "people"
---

```
function(
  plugin_name : string,
  name : string,
  [store : function],
  [finalize : function],
  [supported : function],
  [initialize : function],
  [widget : types.lua_widget]
)
```

This function will add a new storage implemented in Lua.
A storage is a module that is responsible for handling images once they have been generated during export. Examples of core storages include filesystem, e-mail, pwigo...

* **plugin_name** - _string_ - A unique name for the plugin.
* **name** - _string_ - A human readable name for the plugin.
* **\[store\]** - _[function](#store)_ -  This function is called once for each exported image.
* **\[finalize\]** - _[function](#finalize)_ - This function is called once all images are processed and all store calls are finished.
* **\[supported\]** - _[function](#supported)_ - A function called to check if a given image format is supported by the Lua storage.
* **\[initialize\]** - _[function](#initialize)_ - A function called before storage happens.
* **widget** - _[types.lua_widget](../../types/lua_widget)_ - A widget to display in the export section of darktable's UI.

# \[store\]
```
function(
  storage : types.dt_imageio_module_storage_t,
  image : types.dt_lua_image_t,
  format : types.dt_imageio_module_format_t,
  filename : string,
  number : integer,
  total : integer,
  high_quality : boolean,
  extra_data : table
)
```

This function is called once for each exported image. Images can be exported in parallel but the calls to this function will be serialized.

* **storage** - _[types.dt_imageio_module_storage_t](../../types/dt_imageio_module_storage_t)_ - The storage object used for the export.
* **image** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The exported image object.
* **format** - _[types.dt_imageio_module_format_t](../../types/dt_imageio_module_format_t)_ - The format object used for the export.
* **filename** - _string_ - The name of a temporary file where the processed image is stored.
* **number** - _integer_ - The number of the image out of the export series.
* **total** - _integer_ - The total number of images in the export series.
* **high_quality** - _boolean_ - True if the export is high quality.
* **extra_data** - _table_- An empty Lua table to take extra data. This table is common to the initialize, store and finalize calls in an export series.

# \[finalize\]

```
function(
  storage : types.dt_imageio_module_storage_t,
  image_table : table,
  extra_data : table
)
```

This function is called once all images are processed and all store calls are finished.

* **storage** - _[types.dt_imageio_module_storage_t](../../types/dt_imageio_module_storage_t)_ - The storage object used for the export.
* **image_table** - _table_ - A table keyed by the exported image objects and valued with the corresponding temporary export filename.
* **extra_data** - _table_ - An empty Lua table to store extra data. This table is common to all calls to store and the call to finalize in a given export series.


# \[supported\]

```
function(
  storage : types.dt_imageio_module_storage_t,
  format : types.dt_imageio_module_format_t
) : boolean
```

A function called to check if a given image format is supported by the Lua storage; this
is used to build the dropdown format list for the GUI.

Note that the parameters in the format are the ones currently set in the GUI; the user
might change them before export.

* **storage** - _[types.dt_imageio_module_storage_t](../../types/dt_imageio_module_storage_t)_ - The storage object tested.
* **format** - _[types.dt_imageio_module_format_t](../../types/dt_imageio_module_format_t)_ - The format object to report about.
* **return** - _boolean_ - True if the corresponding format is supported.

# \[initialize\]

```
function(
  storage : types.dt_imageio_module_storage_t,
  format : types.dt_imageio_module_format_t,
  images : table of types.dt_lua_image_t,
  high_quality : boolean,
  extra_data : table
) : table or nil
```

A function called before storage happens
This function can change the list of exported functions

* **storage** - _[types.dt_imageio_module_storage_t](../../types/dt_imageio_module_storage_t)_ - The storage object tested.
* **format** - _[types.dt_imageio_module_format_t](../../types/dt_imageio_module_format_t)_ - The format object to report about.
* **images** - _table of [types.dt_lua_image_t](../../types/dt_lua_image_t)_ - A table containing images to be exported.
* **high_quality** - _boolean_ - True if the export is high quality.
* **extra_data** - _table_ - An empty Lua table to take extra data. This table is common to the initialize, store
and finalize calls in an export series.
* **return** - _table or nil_ - The modified table of images to export or nil
If nil (or nothing) is returned, the original list of images will be exported
If a table of images is returned, that table will be used instead. The table can be
empty. The images parameter can be modified and returned
