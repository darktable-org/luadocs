---
title: post-import-film
id: post-import-film
weight: 50
draft: false
author: "people"
---

`event`

This event is triggered when an film import is finished \(all post-import-image callbacks
have already been triggered\). This event can be registered multiple times.

# post-import-film.callback

```
function(
  event : string,
  film : types.dt_lua_film_t
)
```

* **event** - _string_ - The name of the event that triggered the callback.
* **film** - _[types.dt_lua_film_t](../types/dt_lua_film_t)_ - The new film that has been added. If multiple films were added recursively only the top level film is reported.

# post-import-film.extra registration parameters

This event has no extra registration parameters.

