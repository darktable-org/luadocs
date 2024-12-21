---
title: dt_lua_tag_t
id: dt_lua_tag_t
weight: 410
draft: false
author: "people"
---

`dt_type`

A tag that can be attached to an image.

Attributes:

[has_tostring](../attributes#has_tostring)

# dt_lua_tag_t:delete
see [darktable.tags.delete](../../darktable/darktable.tags#darktabletagsdelete)

# dt_lua_tag_t:attach
see [darktable.tags.attach](../../darktable/darktable.tags#darktabletagsattach)

# dt_lua_tag_t:detach
see [darktable.tags.detach](../../darktable/darktable.tags#darktabletagsdetach)

# dt_lua_tag_t.name

`string`

The name of the tag.

# dt_lua_tag_t.flags

`integer`

* 1 - tag is a category
* 2 - tag is private
* 4 - tag has an images order

# dt_lua_tag_t.synonyms

`string`

The synonyms of the tag.

# dt_lua_tag_t.#

[types.dt_lua_image_t](../types/dt_lua_image_t)

The images that have that tag attached to them.

