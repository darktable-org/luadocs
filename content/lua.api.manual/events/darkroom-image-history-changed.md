---
title: darkroom-image-history-changed
id: darkroom-image-history-changed
weight: 12
draft: false
author: "people"
---

`event`

This event is triggered from darkroom view whenever an image's history has changed
and another image is being loaded or darkroom view is being changed to another view.

# darkroom-image-history-changed.callback

```
function(
  event : string,
  image : types.dt_lua_image_t
)
```

* **event** - _string_ - The name of the event that triggered the callback.
* **image** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image loaded into darkroom view

# darkroom-image-history-changed.extra registration parameters

This event has no extra registration parameters.
