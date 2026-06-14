---
title: use_paired_jpg_as_mipmap
id: use_paired_jpg_as_mipmap
weight: 130
draft: false
author: "people"
---

## Name

use_paired_jpg_as_mipmap.lua - use the JPG from the RAW+JPG pair as the full size mipmap

## Description

use_paired_jpg_as_mipmap looks for RAW+JPEG image pairs as images are imported.  After
import the JPEG image is copied to the mipmap cache as the full resolution mipmap. Requests
for smaller mipmap sizes can be satisfied by down sampling the full resolution mipmap.  User's can
decide whether or not to keep the paired JPEG files.  The default is to keep them.  If the 
user doesn't want them, they are deleted after being copied to the mipmap cache.

## Usage

* start this script from script_manager or require it in the user luarc file
* configure the preference to keep or remove the JPEG files

## Additional Software Required

None

## Limitations


## Author

Bill Ferguson - wpferguson@gmail.com

## Change Log
