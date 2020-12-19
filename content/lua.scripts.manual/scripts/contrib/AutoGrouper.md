---
title: AutoGrouper
id: AugoGrouper
weight: 10
draft: false
author: "people"
---

## Name

AutoGrouper.lua - automatically group images based on time

## Description

This plugin groups images based on the time they were shot.  Images shot close
together in time are grouped together.  The interval of time to separate groups
is configurable.

## Usage

Start the module using script manager.

Set a gap amount, in seconds, which will be used to determine when images should no 
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
