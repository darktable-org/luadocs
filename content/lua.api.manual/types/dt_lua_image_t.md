---
title: dt_lua_image_t
id: dt_lua_image_t
weight: 370
draft: false
author: "people"
---

`dt_type`

Image objects represent an image in the database. This is slightly different from a file on
disk since a file can have multiple developments. Note that this is the real image object;
changing the value of a field will immediately change it in darktable and will be reflected
on any copy of that image object you may have kept.

Attributes:

* [has_tostring](../../attributes#has_tostring)

# dt_lua_image_t.attach_tag
see [darktable.tags.attach](../../darktable/darktable.tags#darktabletagsattach)

# dt_lua_image_t.detach_tag
see [darktable.tags.detach](../../darktable/darktable.tags#darktabletagsdetach)

# dt_lua_image_t.get_tags
see [darktable.tags.get_tags](../../darktable/darktable.tags#darktabletagsget_tags)

# dt_lua_image_t.create_style
see [darktable.styles.create](../../darktable/darktable.styles#darktablestylescreate)

# dt_lua_image_t.apply_style
see [darktable.styles.apply](../../darktable/darktable.styles#darktablestylesapply)

# dt_lua_image_t.duplicate
see [darktable.database.duplicate](../../darktable/darktable.database#darktabledatabaseduplicate)

# dt_lua_image_t.move
see [darktable.database.move_image](../../darktable/darktable.database#darktabledatabasemove_image)

# dt_lua_image_t.copy
see [darktable.database.copy_image](../../darktable/darktable.database#darktabledatabasecopy_image)

# dt_lua_image_t.id

`number`

A unique id identifying the image in the database.

# dt_lua_image_t.path

`string`

The file the directory containing the image.

# dt_lua_image_t.film

[types.dt_lua_film_t](../types/dt_lua_film_t)

The film object that contains this image.

# dt_lua_image_t.filename

`string`

The filename of the image.

# dt_lua_image_t.sidecar

`string`

The filename of the image's sidecar file.

# dt_lua_image_t.duplicate_index

`number`

If there are multiple images based on a same file, each will have a unique number, starting
from 0.

# dt_lua_image_t.publisher

`string`

The publisher field of the image.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.title

`string`

The title field of the image.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.creator

`string`

The creator field of the image.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.rights

`string`

The rights field of the image.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.description

`string`

The description field for the image.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.notes

`string`

The notes field for the image.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.version_name

`string`

The version_name field for the image.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.exif_maker

`string`

The maker exif data.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.exif_model

`string`

The camera model used.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.exif_lens

`string`

The id string of the lens used.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.exif_aperture

`number`

The aperture saved in the exif data.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.exif_exposure

`number`

The exposure time of the image.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.exif_focal_length

`number`

The focal length of the image.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.exif_iso

`number`

The iso used on the image.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.exif_datetime_taken

`string`

The date and time of the image.  Milliseconds are shown if the preference *show image time with milliseconds* is enabled.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.exif_focus_distance

`number`

The distance of the subject.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.exif_crop

`number`

The exif crop data.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.latitude

`float or nil`

GPS latitude data of the image, nil if not set.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.longitude

`float or nil`

GPS longitude data of the image, nil if not set.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.elevation

`float or nil`

GPS altitude data of the image, nil if not set.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.is_raw

`boolean`

True if the image is a RAW file.
**WARNING:** This is a flag that gets set the first time the image is opened, either by an edit
or thumbnail generation. If images are imported using darktable.database.import\(\), then
dt_lua_image_t.is_raw is not guaranteed to be correct.

# dt_lua_image_t.is_ldr

`boolean`

True if the image is a ldr image.

# dt_lua_image_t.is_hdr

`boolean`

True if the image is a hdr image.

# dt_lua_image_t.is_altered

`boolean`

True if the image has been edited.

# dt_lua_image_t.has_txt

`boolean`

True if the image has a txt sidecar file.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.width

`number`

The width of the image.

# dt_lua_image_t.height

`number`

The height of the image.

# dt_lua_image_t.final_width

`number`

The final width of the image

# dt_lua_image_t.final_height

`number`

The final height of the image

# dt_lua_image_t.p_width

`number`

The raw width of the image

# dt_lua_image_t.p_height

`number`

The raw height of the image

# dt_lua_image_t.rating

`number`

The rating of the image \(-1 for rejected\).

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.red

`boolean`

True if the image has the corresponding colorlabel.

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.blue
see [types.dt_lua_image_t.red](../types/dt_lua_image_t#dt_lua_image_tred)

# dt_lua_image_t.green
see [types.dt_lua_image_t.red](../types/dt_lua_image_t#dt_lua_image_tred)

# dt_lua_image_t.yellow
see [types.dt_lua_image_t.red](../types/dt_lua_image_t#dt_lua_image_tred)

# dt_lua_image_t.purple
see [types.dt_lua_image_t.red](../types/dt_lua_image_t#dt_lua_image_tred)

# dt_lua_image_t.change_timestamp

`string`

The date and time the image was last edited.

# dt_lua_image_t.reset
```
  self:function(
)
```

Removes all processing from the image, resetting it back to its original state

* **self** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image whose history will be deleted

# dt_lua_image_t.delete
```
self:function(
)
```
Removes an image from the database

* **self** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image to remove

# dt_lua_image_t.group_with
```
self:function(
  [image : types.dt_lua_image_t]
)
```
Puts the first image in the same group as the second image. If no second image is provided
the image will be in its own group.

* **self** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image whose group must be changed.
* **\[image\]** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image we want to group with.

# dt_lua_image_t.make_group_leader
```
self:function(
)
```
Makes the image the leader of its group.

* **self** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image we want as the leader.

# dt_lua_image_t.get_group_members
```
self:function(
) : table of types.dt_lua_image_t
```
Returns a table containing all types.dt_lua_image_t of the group. The group leader is both
at a numeric key and at the "leader" special key \(so you probably want to use ipairs to
iterate through that table\).

* **self** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image whose group we are querying.
* **return** - _table of [types.dt_lua_image_t](../types/dt_lua_image_t)_ - A table of image objects containing all images that are in the same group as the image.

# dt_lua_image_t.group_leader

[types.dt_lua_image_t](../types/dt_lua_image_t)

The image which is the leader of the group this image is a member of.

# dt_lua_image_t.local_copy

`boolean`

True if the image has a copy in the local cache

Attributes:

* [write](../../attributes#write)

# dt_lua_image_t.drop_cache
```
self:function(
)
```
drops the cached version of this image.
This function should be called if an image is modified out of darktable to force darktable to regenerate the thumbnail.
darktable will regenerate the thumbnail by itself when it is needed.

* **self** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image whose cache must be dropped.

# dt_lua_image_t.generate_cache
```
self.function(
  check_dirs : boolean 
  min_size : integer
  max_size : integer
)
```
* **self** - _[types.dt_lua_image_t](../types/dt_lua_image_t)_ - The image whose cache is to be generated.
* **check_dirs** - _boolean_ - check if the mipmap cache directories exist.  Create them if necessary.
* **min_size** - _integer_ - minimum mipmap size to generate
* **max_size** - _integer_ - maximum mipmap size to generate

**NOTES:**
* mipmap cache image sizes
  - 0 - tiny
  - 1 - 180 px
  - 2 - 360 px
  - 3 - 640 px
  - 4 - 1920 px
  - 5 - 2560 px
  - 6 - 4096 px
  - 7 - 5120 px
  - 8 - full resolution

* To generate a single size mipmap image set start_size and end_size to the same value
* When different min_size and max_size sizes are specified, every size mipmap from min_size to max_size is generated.
* When looping over a set of images and generating just one size, check for directories on the first image only.
