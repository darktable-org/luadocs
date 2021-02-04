---
title: darktable.gui.current_view
id: current_view
weight: 40
draft: false
author: "people"
---

```
function(
  [view : types.dt_lua_view_t]
) : types.dt_lua_view_t
```

Get or change the current view.

* **\[view\]** - [_types.dt_lua_view_t](../../types/dt_lua_view_t)_ - The view to switch to. If empty the current view is unchanged
* **return** - [_types.dt_lua_view_t](../../types/dt_lua_view_t)_ - the current view
