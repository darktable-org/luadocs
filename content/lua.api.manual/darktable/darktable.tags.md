---
title: darktable.tags
id: darktable.tags
weight: 230
draft: false
author: "people"
---

Allows access to all existing tags.

# darktable.tags.#

[types.dt_lua_tag_t](../../types/dt_lua_tag_t)

Each existing tag has a numeric entry in the tags table - use ipairs to iterate over them.

### darktable.tags.create

```
function(
  name : string
)
```

Creates a new tag and return it. If the tag exists return the existing tag.

* **name** - _string_ - The name of the new tag.

# darktable.tags.find

```
function(
  name : string
) : types.dt_lua_tag_t
```

Returns the tag object or nil if the tag doesn't exist.

* **name** - _string_ - The name of the tag to find.
* **return** - _
[types.dt_lua_tag_t](../../types/dt_lua_tag_t)_ - The tag object or nil.

# darktable.tags.delete

```
function(
  tag : types.dt_lua_tag_t
)
```

Deletes the tag object, detaching it from all images.

* **tag** - _[types.dt_lua_tag_t](../../types/dt_lua_tag_t)_ - The tag to be deleted.

# darktable.tags.attach

```
function(
  tag : types.dt_lua_tag_t,
  image : types.dt_lua_image_t
)
```

Attach a tag to an image; the order of the parameters can be reversed.

* **tag** - _[types.dt_lua_tag_t](../../types/dt_lua_tag_t)_ - The tag to be attached.
* **image** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The image to attach the tag to.

# darktable.tags.detach

```
function(
  tag : types.dt_lua_tag_t,
  image : types.dt_lua_image_t
)
```

Detach a tag from an image; the order of the parameters can be reversed.

* **tag** - _[types.dt_lua_tag_t](../../types/dt_lua_tag_t)_ - The tag to be detached.
* **image** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The image to detach the tag from.

# darktable.tags.get_tags

```
function(
  image : types.dt_lua_image_t
) : table of types.dt_lua_tag_t
```

Gets all tags attached to an image.

* **image** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The image to get the tags from.
* **return** - _table of [types.dt_lua_tag_t](../../types/dt_lua_tag_t)_ - A table of tags that are attached to the image.

# darktable.tags.get_tagged_images

```
function(
  tag : types.dt_lua_tag_t
) : table of types.dt_lua_image_t
```

Gets all images with the attached tag.

* **tag** - _[types.dt_lua_tag_t](../../types/dt_lua_tag_t)_ - The tag to search images for.
* **return** - _table of [types.dt_lua_image_t](../../types/dt_lua_image_t)_ - A table of images that have the tag attached.
