---
title: darktable.new_format
id: darktable.new_format
weight: 110
draft: false
author: "people"
---

```
function(
type : string
) : types.dt_imageio_module_format_t
```

Creates a new format object to export images

* **type** - _string_ - The type of format object to create, one of :
  * copy
  * exr
  * j2k
  * jpeg
  * pdf
  * pfm
  * png
  * ppm
  * tiff
  * webp

* **return** - _[types.dt_imageio_module_format_t](types.dt_imageio_module_format_t)_ - The newly created object. Exact type depends on the type passed
