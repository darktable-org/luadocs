---
title: group_persistence
id: group_persistence
weight: 55
draft: false
author: "people"
---

## Name

group_persistence.lua - preserve groups between darktable instances

## Description

group_persistence uses "functional" tagging to maintain image groups
across database instances, allowing image grouping to be restored when
the database is rebuilt from the XMP sidecar files.

Once the script is started it "listens" for changes in image grouping and
applies or removes the necessary tags automatically.

A shortcut can be assigned to read a collection and apply the necessary 
grouping tags so that existing collections can be maintained.

If the database is lost and needs to be rebuilt then start the script before
importing any images.  As images are imported the tags will be read and the
grouping applied in the database.

## Usage

* Enable the script using script manager
* Optionally, create a keystroke combination for the shortcut

## Additional Software Required

None

## Limitations

In normal use you wont notice that the script is running.

However if you do something like import 4000+ images, then
run the autogrouper script to create groups whenever there is
a 5 second difference between 2 images, your system will be busy
for awhile.  If for some reason you need to do something like this
turn off group_persistence, run the autogrouper, turn on group_persistence
and use the shortcut to read all the grouping information and apply
the necessary tags.  It will still be an impact, but less than trying
to do both at once.  Learned from experience :-)

## Author

Bill Ferguson - wpferguson@gmail.com

## Change Log
