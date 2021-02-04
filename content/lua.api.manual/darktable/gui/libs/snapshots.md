---
title: darktable.gui.libs.snapshots
id: snapshots
weight: 340
draft: false
author: "people"
---

The UI element that manipulates snapshots in darkroom

Attributes:
* [has_tostring](../../../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../../types/dt_lua_lib_t)

## darktable.gui.libs.snapshots.ratio

number - The place in the screen where the line separating the snapshot is. Between 0 and 1

Attributes:
* [write](../../../Attributes#write)

darktable.gui.libs.snapshots.direction

[types.snapshot_direction_t](../../../types/snapshot_direction_t) - The direction of the snapshot overlay

Attributes:
* [write](../../../Attributes#write)

## darktable.gui.libs.snapshots.#

[types.snapshot_direction_t](../../../types/snapshot_direction_t) - The different snapshots for the image

## darktable.gui.libs.snapshots.selected

[types.snapshot_direction_t](../../../types/snapshot_direction_t) - The currently selected snapshot

## darktable.gui.libs.snapshots.take_snapshot

```
function(
)
```

Take a snapshot of the current image and add it to the UI
The snapshot file will be generated at the next redraw of the main window

## darktable.gui.libs.snapshots.max_snapshot

number - The maximum number of snapshots

