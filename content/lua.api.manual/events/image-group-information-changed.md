---
title: image-group-information-changed
id: image-group-information-changed
weight: 42
draft: false
author: "people"
---

`event`

This event is called when image grouping information changes.

# image-group-information-changed.callback

```
function(
  event : string,
  reason : string,
  image : types.dt_lua_image_t,
  group_leader : types.dt_lua_image_t
)
```

* **event** - _string_ - The name of the event that triggered the callback.
* **reason** - _string_ - The reason grouping changed.  One of add, remove, leader-change, remove-leader.
* **image** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image object that the change applies to.
* **group_leader** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image object that is the group leader

# image-group-information-changed.extra registration parameters

This event has no extra registration parameters.

