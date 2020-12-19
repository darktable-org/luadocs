---
title: autostyle
id: autostyle
weight: 20
draft: false
author: "people"
---

## Name

autostyle.lua - automatically apply a given style when an exif tag is present in the image file

## Description

Automatically apply a given style when an exif tag is present in the file. This tags are checked with exiftool, in order to be able to match very exotic tags.
This was written to be able to apply a style to compensate for Auto-DR from Fujifilm cameras.

## Usage

* Set the exif configuration string in your lua configuration.
  For instance,  _AutoDynamicRange=200%=>DR200_
  means that I automatically want to apply my DR200 style on all
  images where exiftool returns "200%"" for the AutoDynamicRange tag

* If you want to be able to apply it to already imported
  images, define a shortcut (lua shortcuts). If the history stack is 
  removed from the image, autostyle won't be applied again.
  This shortcut useful when that happens.

* Import your images, or use the shortcut on already imported images

* To determine which tag you want, list all tags with exiftool:
  `exiftool -j XE021351.RAF`, and find the one you want to use.
  You can check tags with 
  ```
  > exiftool -AutoDynamicRange XE021351.RAF
  Auto Dynamic Range              : 200%
  ```

## Additional Software Required

* exiftool

## Limitations


## Author

Marc Cousin - cousinmarc@gmail.com

## Change Log
