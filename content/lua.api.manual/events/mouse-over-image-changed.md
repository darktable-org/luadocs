---
title: mouse-over-image-changed
id: mouse-over-image-changed
weight: 90
draft: false
author: "people"
---

`event`

This event is triggered whenever the image under the mouse changes

# mouse-over-image-changed.callback

```
function(
  event : string,
  image : types.dt_lua_image_t
)
```

* **event** - _string_ - The name of the event that triggered the callback.
* **image** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The new image under the mouse, can be nil if there is no image under the mouse

# mouse-over-image-changed.extra registration parameters

This event has no extra registration parameters.

