---
title: CollectHelper
id: CollectHelper
weight: 40
draft: false
author: "people"
---

## Name

CollectHelper.lua - add buttons to help with collections

## Description

This plugin adds the button(s) to the "Selected Images" module:
1) Return to Previous Collection
2) Collect on image's Folder
3) Collect on image's Color Label(s)
4) Collect on All (AND)

It also adds 3 preferences to the lua options dialog box which allow the user to activate/deactivate the 3 "Collect on" buttons.

Button Behavior:
1) Return to Previous Collection - Will reset the collect parameters to the previously active settings
2) Collect on image's Folder - Will change the collect parameters to be "Folder" with a value of the selected image's folder location
3) Collect on image's Color Label(s) - Will change the collect parameter to be "Color" with a value of the selected images color labels, will apply multiple parameters with AND logic if multiple exist
4) Collect on All (AND) - Will collect on all parameters activated by the preferences dialog, as such this button is redundant if you only have one of the two other options enabled

## Usage

* start CollectHelper with script manager.

* Select the photo you wish to change you collection based on.
  In the "Selected Images" module click on "Collect on this Image"

## Additional Software Required


## Limitations


## Author

Kevin Ertel

## Change Log
