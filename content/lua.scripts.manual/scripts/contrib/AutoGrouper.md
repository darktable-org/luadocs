---
title: AugoGrouper
id: AugoGrouper
weight: 10
draft: false
author: "people"
---

## Name

AugoGrouper.lua - add the module "Auto Group" to darktable's lighttable view

## Description

This plugin adds the module "Auto Group" to darktable's lighttable view

## Usage

Install: (see here for more detail: https://github.com/darktable-org/lua-scripts )
 1) Copy this file in to your "lua/contrib" folder where all other scripts reside. 
 2) Require this file in your luarc file, as with any other dt plug-in

Set a gap amount in second which will be used to determine when images should no 
longer be added to a group. If an image is more then the specified amount of time
from the last image in the group it will not be added. Images without timestamps 
in exif data will be ignored.

There are two buttons. One allows the grouping to be performed only on the currently
selected images, the other button performs grouping on the entire active collection

## Additional Software Required


## Limitations


## Author

Kevin Ertel

## Change Log
