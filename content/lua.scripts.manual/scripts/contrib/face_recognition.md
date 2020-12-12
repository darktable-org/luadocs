---
title: face_recognition
id: face_recognition
weight: 100
draft: false
author: "people"
---

## Name

face_recognition.lua - add a new storage option and calls face_recognition after export

## Description

Add a new storage option to send images to face_recognition.
Images are exported to darktable tmp dir first.
A directory with known faces must exist, the image name are the
tag names which will be used.
Multiple images for one face can exist, add a number to it, the
number will be removed from the tag, for example:
People|IknowYou1.jpg
People|IknowYou2.jpg
People|Another.jpg
People|Youtoo.jpg

## Usage

* require this file from your main luarc config file.

## Additional Software Required

* https://github.com/ageitgey/face_recognition
* https://github.com/darktable-org/lua-scripts/tree/master/lib

## Limitations


## Author

Sebastian Witt

## Change Log
