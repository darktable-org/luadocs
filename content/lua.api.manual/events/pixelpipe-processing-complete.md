---
title: pixelpipe-processing-complete
id: pixelpipe-processing-complete
weight: 65
draft: false
author: "people"
---

`event`

This event is triggered when a pixelpipe processing run is complete.

# pixelpipe-processing-complete.callback

```
function(
  event : string,
  image : types.dt_lua_image_t
)
```

* **event** - _string_ - The name of the event that triggered the callback.
* **image** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image loaded into darkroom view

# pixelpipe-processing-complete.extra registration parameters

This event has no extra registration parameters.
