---
title: post-import-image
id: post-import-image
weight: 30
draft: false
author: "people"
---

`event`

This event is triggered whenever a new image is imported into the database. This event
can be registered multiple times, all callbacks will be called. The call is blocking.

# post-import-image.callback

```
function(
  event : string,
  image : types.dt_lua_image_t
)
```

* **event** - _string_ - The name of the event that triggered the callback.
* **image** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image object that has been imported.

# post-import-image.extra registration parameters

This event has no extra registration parameters.

