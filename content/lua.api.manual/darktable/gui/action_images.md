---
title: darktable.gui.action_images
id: action_images
weight: 20
draft: false
author: "people"
---
\
`table`

A table of [types.dt_lua_image_t](../../types/dt_lua_image_t) on which the user expects UI actions to happen.
It is based on both the hovered image and the selection and is consistent with the way
darktable works.
It is recommended to use this table to implement Lua actions rather than [darktable.gui.hovered](hovered.md) or [darktable.gui.selection](selection.md) to be consistent with darktable's GUI.

