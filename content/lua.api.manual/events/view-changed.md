---
title: view_changed
id: view_changed
weight: 60
draft: false
author: "people"
---

`event`

This event is triggered after the user changed the active view

#view-changed.callback

```
function(
  event : string,
  old_view : types.dt_lua_view_t,
  new_view : types.dt_lua_view_t
)
```

* **event** - _string_ - The name of the event that triggered the callback.
* **old_view** - _[types.dt_lua_view_t](../types/dt_lua_view_t)_ - The view that we just left
* **new_view** - _[types.dt_lua_view_t](../types/dt_lua_view_t)_ - The view we are now in

#view-changed.extra registration parameters

This event has no extra registration parameters.

