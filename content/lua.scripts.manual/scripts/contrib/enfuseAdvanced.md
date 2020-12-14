---
title: enfuseAdvanced
id: enfuseAdvanced
weight: 70
draft: false
author: "people"
---

## Name

enfuseAdvanced.lua - process HDR or focus stacked images

## Description

This plugin will add the new export module 'fusion to DRI or DFF image'.

## Usage

Install:
 1) Get the Lua scripts: https://github.com/darktable-org/lua-scripts#download-and-install
 2) Require this file in your luarc file, as with any other dt plug-in: require "contrib/enfuseAdvanced"
 3) Then select "DRI or DFF image" as storage option
 4) On the initial startup set your executable paths 

DRI = Dynamic Range Increase (Blend multiple bracket images into a single LDR file)
DFF = Depth From Focus ('Focus Stacking' - Blend multiple images with different focus into a single image)
Select multiple images that are either bracketed, or focus-shifted, set your desired operating parameters, and press the export button. A new image will be created. The image will
be auto imported into darktable if you have that option enabled. Additional tags or style can be applied on auto import as well, if you desire.

image align options:
See align_image_stack documentation for further explanation of how it specifically works and the options provided (http://hugin.sourceforge.net/docs/manual/Align_image_stack.html)

image fustion options:
See enfuse documentation for further explanation of how it specifically works and the options provided (https://wiki.panotools.org/Enfuse)
If you have a specific set of parameters you frequently like to use, you can save them to a preset. There are 3 presets available for DRI, and 3 for DFF.

target file:
Select your file destination path, or check the 'save to source image location' option.
'Create Unique Filename' is enabled by default at startup, the user can choose to overwrite existing
Set any tags or style you desire to be added to the new image (only available if the auto-import option is enabled). You can also change the defaults for this under settings > lua options

format options:
Same as other export modules

global options:
Same as other export modules

## Additional Software Required

align_image_stack
enfuse ver. 4.2 or greater
exiftool

## Limitations


## Author

Kevin Ertel

## Change Log
