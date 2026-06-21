---
title: selection2collection
id: selection2collection
weight: 118
draft: false
author: "people"
---

## Name

selection2collection.lua - create a temporary collection from a selection

## Description

selection2collection creates a temporary collection, using functional
tagging, from a selection. The collection lasts until darktable exits
and then the collections are removed, but not the images.

To create the temporary collection, a function tag (darktable|functional|s2c) 
tag with a date and a time is applied to the selected images.  The collection
module filters on the tag to display the connection.  More than one temporary
collection can be created and collections can be changed by selecting the 
appropriate tag.

The tags are autmatically destroyed when darktable exits, thus removing the
collections.  There is a preference in the Lua options to keep the collections
across darktable runs.

## Usage

* start this script from script_manager or require it in the user luarc file
* make a selection
* click the create temporary collection button the the actions on selected images
module

## Additional Software Required

None

## Limitations


## Author

Bill Ferguson - wpferguson@gmail.com

## Change Log
