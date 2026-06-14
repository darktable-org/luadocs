---
title: extract_burst_roll_images
id: extract_burst_roll_images
weight: 55
draft: false
author: "people"
---

## Name

extract_burst_roll_images.lua - extract burst images from a burst roll file

## Description

Canon cameras are capable of shooting in burst mode.  When the shutter
button is half pressed the camera starts "recording".  When the shutter is
fully pressed the previous 1/2 second of imformation is recorded as individual
images stored in one file as well as images captured at 30 frames/sec until
the buffer fills or the shutter button is released.  So a Canon R7 burst file
could contain ~90 images.

Extracting the images from this file required use of Canon proprietary software
until recently when dnglab got the capability to extract the embedded images as
DNG raws.

This script can be set to run on import, scanning for burst roll containers,
extracting the embedded images and grouping them with the burst roll container image.
The script can alsu be utilized via a shortcut and applied to selected images.  It's recommended
to use the shortcut instead of on import if you are shooting a lot of burst roll images as they
can quickly fill a disk when extracted.

When set to on import the script scans each image after import using internal metadata if available or exiv2 or exiftool
to check the image EXIF information to see if the file is a busrt roll container.
Once the import images are scanned, the detected burst roll containers are processed,
the embedded images extracted as DNSs, and grouped with the container image.

In shortcut mode the user selects the burst roll containers manually and uses the shortcut
to extract the embedded images as DNGs

## Usage

* start the script from script_manager or require it in the user luarc file
* add the Exif.Canon.RawBurstModeRoll tag to the metadata editor module
* set the preferences in perferences->Lua options

## Additional Software Required

* exiv2    - https://exiv2.org - not required if internal metadata used
* exiftool - https://exiftool.org - not required if internal metadata used
* dnglab   - https://github.com/dnglab/dnglab

## Limitations

extract_burst_roll_images makes heavy use of external programs to identify burst roll
containters and to extract the images.  Windows users may want to use it in shortcut mode
to lessen the number of windows popping up.

## Author

Bill Ferguson - wpferguson@gmail.com

## Change Log
