---
title: find_image_by_id
id: find_image_by_id
weight: 35
draft: false
author: "people"
---

## NAME

find_image_by_id

## SYNOPSIS

look up an image by ID in the database

## USAGE
```
local du = require "lib/dtutils"
local img = du.find_image_by_id(imgid)
```
**imgid** - int - the image ID to retrieve  

## DESCRIPTION

**find_image_by_id** looks up an image by ID in the database.

## RETURN VALUE

**img** - _[dt_lua_image_t](../../../lua.api.manual/types/dt_lua_image_t.md)_ - image with the given ID if found, nil if not

