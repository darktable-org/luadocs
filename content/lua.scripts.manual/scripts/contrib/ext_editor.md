---
title: ext_editor
id: ext_editor
weight: 90
draft: false
author: "people"
---

## Name

ext_editor.lua - edit images with external editors

## Description

This script provides helpers to edit image files with programs external to darktable. It adds:
- a new target storage "collection". Image exported will be reimported to collection for further editing with external programs
- a new lighttable module "external editors", to select a program from a list of up to
9 external editors and run it on a selected image (adjust this limit by changing MAX_EDITORS)
- an option to display the module in darkroom view
- a set of lua preferences in order to configure name and path of up to 9 external editors
- a set of lua shortcuts in order to quick launch the external editors

## Usage

* start this script with script manager
  
### setup

* in "preferences/lua options" configure name and path/command of external programs
* note that if a program name is left empty, that and all following entries will be ignored
* in "preferences/shortcuts/lua" configure shortcuts for external programs (optional)
* whenever programs preferences are changed, in lighttable/external editors, press "update list"

### use

* in the export dialog choose "collection" and select the format and bit depth for the
   exported image
* press "export"
* the exported image will be imported into collection and grouped with the original image
      
* in lighttable, select an image for editing with en external program 
(or in darkroom for the image being edited):
* in external editors GUI, select program and press "edit"
* edit the image with the external editor, overwite the file, quit the external program
* the selected image will be updated
  or
* in lighttable/external editors, select program and press "edit a copy"
* edit the image with the external editor, overwite the file, quit the external program
* a copy of the selected image will be created and updated
  or
* in lighttable select target storage "collection"
* enter in darkroom
* to create an export or a copy press CRTL+E
* use the shortcut to edit the current image with the corresponding external editor
* overwite the file, quit the external program
* the darkroom view will be updated
    
* warning: mouseover on lighttable/filmstrip will prevail on current image
* this is the default DT behavior, not a bug of this script


## Additional Software Required


## Limitations

* MAC compatibility not tested

## Author

Marco Carrarini - marco.carrarini@gmail.com

## Change Log
