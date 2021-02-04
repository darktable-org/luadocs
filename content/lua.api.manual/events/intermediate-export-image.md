---
title: intermediate-export-image
id: intermediate-export-image
weight: 50
draft: false
author: "people"
---

`event`

This event is called each time an image is exported, once for each image after the image
has been processed to an image format but before the storage has moved the image to
its final destination. The call is blocking.

# intermediate-export-image.callback

```
function(
  event : string,
  image : types.dt_lua_image_t,
  filename : string,
  format : types.dt_imageio_module_format_t,
  storage : types.dt_imageio_module_storage_t
)
```

* **event** - _string_ - The name of the event that triggered the callback.
* **image** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image object that has been exported.
* **filename** - _string_ - The name of the file that is the result of the image being processed.
* **format** - _[types.dt_imageio_module_format_t](../types/dt_imageio_module_format_t)_ - The format used to export the image.
* **storage** - _[types.dt_imageio_module_storage_t](../types/dt_imageio_module_storage_t)_ - The storage used to export the image \(can be nil\).

# intermediate-export-image.extra registration parameters

This event has no extra registration parameters.

