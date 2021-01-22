---
title: darktable.database
id: darktable.database
weight: 180
draft: false
author: "people"
---

Allows access to the database of images. Note that duplicate images \(images with the
same RAW but different XMP\) will appear multiple times with different duplicate indexes.
Also note that all images are here. This table is not influenced by any GUI filtering \(collections, stars etc...\).

# darktable.database.#

[types.dt_lua_image_t](../../types/dt_lua_image_t)

Each image in the database appears with a numerical index; you can iterate over them using
ipairs.

# darktable.database.duplicate

```
function(
  image : types.dt_lua_image_t
) : types.dt_lua_image_t
```

Creates a duplicate of an image and returns it.

* **image** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - the image to duplicate
* **return** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The new image object.

# darktable.database.import

```
function(
  location : string
) : types.dt_lua_image_t
```

Imports new images into the database.

* **location** - _string_ - The filename or directory to import images from. NOTE: If the images are set to be
imported recursively in preferences only the toplevel film is returned \(the one whose
path was given as a parameter\). NOTE 2: If the parameter is a directory the call is nonblocking; the film object will not have the newly imported images yet. Use a [post-import-film](..//../events/post-imort-film) filtering on that film to react when images are actually imported.
* **return** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The created image if an image is imported or the toplevel film object if a film was
imported.

# darktable.database.get_image

**Lua API 6.2.0**

```
function(
  image_id : int,
) : types.dt_lua_image_t
```

Get an image, specified by image_id, from the database.

* **image_id** - _int_ - The id number of the image to get
* **return** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The image object if found, otherwise nil

# darktable.database.move_image

```
function(
  image : types.dt_lua_image_t,
  film : types.dt_lua_film_t,
  [newname : string]
)
```

Physically moves an image \(and all its duplicates\) to another film, and/or renames the image file.
This will move the image file, the related XMP and all XMP for the duplicates to the directory of the new film and rename them as specified.
Note that the order of the two required parameters is not relevant.

* **image** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The image to move
* **film** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The film to move to. To rename a file within the same film, set this to the image's
current film.
* **\[newname\]** - _string_ - \(Optional\) If provided, rename the file with this new name. Must not contain any path
separator characters.

# darktable.database.copy_image

```
function(
  image : types.dt_lua_image_t,
  film : types.dt_lua_film_t,
  [newname : string]
) : types.dt_lua_image_t
```

Physically copies an image to another film.
This will copy the image file and the related XMP to the directory of the new film and
rename them as specified.
If there is already a file with the same name as the image file, it will create a duplicate
from that file instead.
Note that the order of the two required parameters is not relevant.

* **image** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The image to copy
* **film** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The film to copy to. To make a copy of a file within the same film, set this to the image's
current film.
* **\[newname\]** - _string_ - \(Optional\) If provided, give the copy this new filename. Must not contain any path separator characters.
* **return** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The new image

# darktable.database.delete
see [types.dt_lua_image_t.delete](../../types/dt_lua_image_t.delete)
