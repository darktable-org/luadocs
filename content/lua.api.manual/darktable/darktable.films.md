---
title: darktable.films
id: darktable.films
weight: 70
draft: false
author: "people"
---

A table containing all the film objects in the database.

# darktable.films.#

`types.dt_lua_film_t`

Each film has a numeric entry in the database.  See [types.dt_lua_film_t](../../types/dt_lua_film_t).

# darktable.films.new

```
function(
  directory : string
) : types.dt_lua_film_t
```

Creates a new empty film

see [darktable.database.import](../darktable/database#import) to import a directory with all its images and to add images
to a film

* **directory** - _string_ - The directory that the new film will represent. The directory must exist
* **return** - _[types.dt_lua_film_t](../../types/dt_lua_film_t)_ - The newly created film, or the existing film if the directory is already imported

# darktable.films.delete

see [types.dt_lua_film_t](../../types/dt_lua_film_t)

