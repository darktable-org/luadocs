---
title: import_filter_manager
id: import_filter_manager
weight: 80
draft: false
author: "people"
---

## Name

import_filter_manager.lua - add a dropdown list with import filters to the import dialog

## Description

This script adds a dropdown list with import filters to the import dialog.
Scripts can add new filters by registering them with
  darktable.register_import_filter(name, callback)
The callback has type function(event, images), i.e., it is the same as when
directly registering the pre-import event.

## Usage

* start this script from script manager
* also require some files with import filters, for example import_filters.lua.
  it is important to add them AFTER this one!

## Additional Software Required


## Limitations


## Author

Tobias Ellinghaus

## Change Log
