---
title: darktable.collection
id: darktable.collection
weight: 180
draft: false
author: "people"
---

Allows to access the currently worked on images, i.e the ones selected by the collection
lib. Filtering \(rating etc\) does not change that collection.

# darktable.collection.#

[types.dt_lua_image_t](../../types/dt_lua_image_t)

Each image in the collection appears with a numerical index; you can iterate them using
ipairs.
