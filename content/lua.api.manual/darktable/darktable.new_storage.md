---
title: darktable.new_storage
id: darktable.new_storage
weight: 90
draft: false
author: "people"
---

```
function(
type : string
) : types.dt_imageio_module_storage_t
```

Creates a new storage object to export images.

* **type** - _string_ - The type of storage object to create, one of:
  * disk
  * email
  * gallery
  * latex
  * piwigo
  * \(Other, lua-defined, storage types may appear.\)

* **return** - _[types.dt_imageio_module_storage_t(../../types/dt_imageio_module_storage_t)]_ - The newly created object. Exact type depends on the type passed

