---
title: darkroom-image-loaded
id: darkroom-image-loaded
weight: 15
draft: false
author: "people"
---

`event`

This event is triggered whenever an image is loaded in darkroom view

# darkroom-image-loaded.callback

```
function(
  event : string,
  image : types.dt_lua_image_t
)
```

* **event** - _string_ - The name of the event that triggered the callback.
* **image** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image loaded into darkroom view

# darkroom-image-loaded.extra registration parameters

This event has no extra registration parameters.
