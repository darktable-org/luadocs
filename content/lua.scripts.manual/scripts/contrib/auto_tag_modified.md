---
title: auto_tag_modified
id: auto_tag_modified
weight: 17
draft: false
author: "people"
---

## Name

auto_tag_modified.lua - automatically automatically tag an image when it has been manually modified in darkroom

## Description

This plugin automatically tags an image when it has been manually modified in darkroom
so that it is easier to tell manually edited images apart from images which had automatic modifications done to them.

## Usage

Start the module using script manager.

Open an image in darkroom, and close it after making an operation that changes the history

### Preferences

Once the script is enabled, the tag name which gets applied to modified images can be changes in the Lua option in darktable's preferences. The default tag name is `darktable manually modified`.

## Additional Software Required


## Limitations

The script will only catch modifications done in darkroom. Other modifications, for example manually applying a style or copying a history stack, will not be detected and therefore not tagged.

## Author

Michael Reiger - michael@rauschpfeife.net

## Change Log
