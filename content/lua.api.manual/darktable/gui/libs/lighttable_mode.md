---
title: darktable.gui.libs.lighttable_mode
id: lighttable_mode
weight: 190
draft: false
author: "people"
---

The navigation and zoom level UI in lighttable

Attributes:
* [has_tostring](../../../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../../types/dt_lua_lib_t)

## darktable.gui.libs.lighttable_mode.layout

```
function(
  [layout : types.dt_lighttable_layout_t]
) : types.dt_lighttable_layout_t
```

Change the lighttable layout.

* **\[layout\]** - _[types.dt_lighttable_layout_t](../../../types/dt_lighttable_layout_t)_ - The layout to switch to. If empty the current layout is unchanged
* **return** - _[types.dt_lighttable_layout_t](../../../types/dt_lighttable_layout_t)_ - the current layout

## darktable.gui.libs.lighttable_mode.zoom_level

```
function(
  [level : int]
) : int
```

Change the lighttable zoom level.

* **\[level\]** - _int_ - The zoom level to switch to. If empty the current zoom level is unchanged
* **return** - _int_ - the current zoom level

