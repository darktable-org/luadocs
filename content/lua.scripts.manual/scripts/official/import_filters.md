---
title: import_filters
id: import_filters
weight: 90
draft: false
author: "people"
---

## Name

import_filters.lua - add filters for [import_filter_manager](import_filter_manager.md)

## Description

This script goes along with the import filter manager. It adds two filters:
* ignore jpegs: this one does the same as the existing option in the import dialog
                and just skips all JPEGs during import.
* prefer raw over jpeg: this one is a bit more elaborate, it ignores JPEGs when there
                        is also another file with the same basename, otherwise it
                        allows JPEGs, too.

## Usage

* start this script from script manager AFTER import_filter_manager.lua

## Additional Software Required


## Limitations


## Author

Tobias Ellinghaus & Christian Mandel

## Change Log
