---
title: dt_lua_film_t
id: dt_lua_film_t
weight: 240
draft: false
author: "people"
---

`dt_type`

A film in darktable; this represents a directory containing imported images.

Attributes:

* [has_tostring](../attributes#has_tostring)

# dt_lua_film_t.move_image
see [darktable.database.move_image](../../darktable/darktable.database#darktabledatabasemove_image)

# dt_lua_film_t.copy_image
see [darktable.database.copy_image](../../darktable/darktable.database#darktabledatabasecopy_image)

# dt_lua_film_t.#

[types.dt_lua_image_t](../types/dt_lua_image_t)

The different images within the film.

# dt_lua_film_t.id

`number`
A unique numeric id used by this film.

Attributes:

* [write](../attributes#write)

# dt_lua_film_t.path

`string`

The path represented by this film.

Attributes:

* [write](../attributes#write)

# dt_lua_film_t.delete
```
self:function(
  [force : boolean]
)
```

Removes the film from the database.

* **self** - _[types.dt_lua_film_t](../types/dt_lua_film_t)_ - The film to remove.
* **\[force\]** - _boolean_ - Force removal, even if the film is not empty.

