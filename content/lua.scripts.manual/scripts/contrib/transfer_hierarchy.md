---
title: transfer_hierarchy
id: transfer_hierarchy
weight: 320
draft: false
author: "people"
---

## Name

transfer_hierarchy.lua - move or copy image hierarchies from one location to another

## Description

Allows the moving or copying of images from one directory
tree to another, while preserving the existing hierarchy.

## Usage

darktable's native operations for moving and copying images in
batches allow only one directory to be specified as the destination
for each batch. Those wanting to move or copy images from a _hierarchy_
of directories within darktable while preserving the directory structure,
must take the laborious step of performing the operation one individual
directory at a time.

This module allows the intact moving and copying of whole directory trees.
It was designed for the specific use case of rapidly transferring images
from a customary source (e.g., a staging directory on the local disk)
to a customary destination (e.g., a directory on a NAS device).

Instructions for operation:

1. Select the set of images you want to copy.

2. Click the "calculate" button. This will calculate the
   lowest directory in the hierarchy that contains every selected
   file (i.e., the common prefix of all the images' pathnames), and
   write its path into the "existing root" text box.

3. If (a) you have specified the "customary source root" and "customary
   destination root" preferences, and (b) the selected images are all
   contained under the directory specified as the customary source
   root, then the "root of destination" text box will also be
   automatically filled out.

   For example, suppose that you have specified '/home/user/Staging'
   as your customary source root and '/mnt/storage' as your customary
   destination root. If all selected images fell under the directory
   '/home/user/Staging/2020/Roll0001', the "root of destination" would
   be automatically filled out with '/mnt/storage/2020/Roll0001'.

   But if all selected images fall under a directory outside the
   specified customary source root (e.g., '/opt/other'), the "root
   of destination" text box must be filled out manually.

   It is also possible to edit the "root of destination" further once
   it has been automatically filled out.

4. Click the "move" or "copy" button.

   Before moving or copying any images, the module will first
   replicate the necessary directory hierarchy by creating all
   destination directories that do not already exist; should a
   directory creation attempt fail, the operation will be
   aborted, but any directories already created will not be
   removed.

   During the actual move/copy operation, the module transfers an
   image by taking its path and replacing the string in the "existing
   root" text box with that in the "root of destination" text box
   (e.g., '/home/user/Staging/2020/Roll0001/DSC_0001.jpg' would be
   transferred to '/mnt/storage/2020/Roll0001/DSC_0001.jpg').

## Additional Software Required


## Limitations


## Author

August Schwerdfeger - august@schwerdfeger.name
