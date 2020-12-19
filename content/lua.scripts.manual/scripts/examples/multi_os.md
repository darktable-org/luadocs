---
title: name
id: name
weight: 70
draft: false
author: "people"
---

## Name

multi_os.lua - an example script that runs on linux, MacOS, and Windows.

## Description

multi_os is an example of how to write a script that will run on different
operating systems.  It uses the lua-scripts libraries to lessen the amount
of code that needs to be written, as well as gaining access to tested 
cross-platform routines.  This script also performs a function that some 
may find useful.  It creates a button in the lighttable selected images module
that extracts the embedded jpeg image from a raw file, then imports it and groups
it with the raw file.  A keyboard shortcut is also created.  A key combination can
be assigned to the shortcut in the lua preferences and then the action can be invoked
by hovering over the image and pressing the key combination.

## Usage

* start this script from script manager
* start darktable, open prefreences, go to lua options and update the executable location if you are running Windows or MacOS, then restart darktable.
* select an image or images
* click the button to extract the jpeg

## Additional Software Required

* ufraw-batch - https://ufraw.sourceforge.net
                MacOS - install with homebrew

## Limitations


## Author

Bill Ferguson - wpferguson@gmail.com

## Change Log
