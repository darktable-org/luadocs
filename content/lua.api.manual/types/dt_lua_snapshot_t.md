---
title: dt_lua_snapshot_t
id: dt_lua_snapshot_t
weight: 400
draft: false
author: "people"
---

`dt_type`

The description of a snapshot in the snapshot lib

Attributes:

[has_tostring](../attributes#has_tostring)

# dt_lua_snapshot_t.filename

`string`

The filename of an image containing the snapshot

# dt_lua_snapshot_t:select
```
self:function(
)
```
Activates this snapshot on the display. To deactivate all snapshot you need to call this
function on the active snapshot

* **self** - _[types.dt_lua_snapshot_t](../types/dt_lua_snapshot_t)_ - The snapshot to activate

# dt_lua_snapshot_t.name

`string`

The name of the snapshot, as seen in the UI

