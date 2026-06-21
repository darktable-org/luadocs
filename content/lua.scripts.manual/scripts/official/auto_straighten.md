---
title: auto_straighten
id: auto_straighten
weight: 7
draft: false
author: "people"
---

## Name

auto_straighten.lua - straighten an image in darkroom using image metadata

## Description

auto_straighten reads the roll and pitch angle imformation recorded when
an image is captured.  A correction is computed and applied to correct the 
roll to the nearest vertical or horizontal axis using the rotate and 
perspective module.

The roll and pitch angle metadata field can be added to the metadata editor
module which will then populate the field when an image is imported and make
it available internally to the script.  Otherwise, the exiftool external
executable must be used to get the data.

## Usage

* start this script from script_manager or require it from the user luarc

## Additional Software Required

* exiftool - https://exiftool.org

## Limitations

* Roll and pitch angles are taken when an image is captured.  If you shoot
in burst mode, the roll and pitch angles of the first image are used in
the rest of the burst (at least for Canon).
* If you are running multiple scripts that trigger on an image being opened
in darkroom then the auto crop may not work.  There is a shortcut included
that can have a key sequence assigned so that the auto crop will be reapplied.
* Currently only roll angle is corrected

## Author

Bill Ferguson - wpferguson@gmail.com

## Change Log
