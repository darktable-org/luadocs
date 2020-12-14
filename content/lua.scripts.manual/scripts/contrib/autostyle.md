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

Automatically apply a given style when an exif tag is present in the file. This tagged is checked with exiftool, in order to be able to match very exotic tags.
I wrote this initially to be able to apply a style to compensate for Auto-DR from my Fujifilm camera

## Usage

* set the exif configuration string in your lua configuration
  mine, for instance, is AutoDynamicRange=200%=>DR200"
  meaning that I automatically want to apply my DR200 style on all
  images where exiftool returns '200%' for the AutoDynamicRange tag
* if you want to be able to apply it manually to already imported
  images, define a shortcut (lua shortcuts). As I couldn't find an event for
  when a development is removed, so the autostyle won't be applied again, 
  this shortcut is also helpful then
* import your images, or use the shortcut on your already imported images
* To determine which tag you want, list all tags with exiftool:
  exiftool -j XE021351.RAF, and find the one you want to use
  you can check it with 
  > exiftool -AutoDynamicRange XE021351.RAF
  Auto Dynamic Range              : 200%

## Additional Software Required

* exiftool

## Limitations


## Author

Marc Cousin - cousinmarc@gmail.com

## Change Log
