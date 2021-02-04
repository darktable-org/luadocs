---
title: darktable.gui.selection
id: selection
weight: 140
draft: false
author: "people"
---

```
function(
  [selection : table of types.dt_lua_image_t]
) : table of types.dt_lua_image_t
```

Get or change the set of selected images.

Attributes: [implicit_yield](../Attributes#implicit_yield)

* **\[selection\]** - _table of [types.dt_lua_image_t](../../types/dt_lua_image_t)_ - A table of images which will define the selected images. If this parameter is not given
the selection will be untouched. If an empty table is given the selection will be emptied.
* **return** - _table of [types.dt_lua_image_t](../../types/dt_lua_image_t)_ - A table containing the selection as it was before the function was called.
