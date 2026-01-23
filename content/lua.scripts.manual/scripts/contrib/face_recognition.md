---
title: face_recognition
id: face_recognition
weight: 100
draft: false
author: "people"
---

## Name

face_recognition.lua - Calls externel tool [face_recognition]() and applies the results

## Description

Adds on option to apply face recognition on a selection of photos. The results are written into customizable tags.

## Preparation

1. Install the face recognition solution https://github.com/ageitgey/face_recognition: `pipx install face-recognition`
2. Prepare your known faces in the following fashion:

You need a directory which holds the photos of all known faces. The file names are the tag names which will be used. You can add a number suffix to provide multiple photos of the same persone to improve the result. The number will be removed from the tag.

Example:

- `People|Family|IknowYou1.jpg`
- `People|Family|IknowYou2.jpg`
- `People|Friend|Another.jpg`
- `People|Youtoo.jpg`

3. Enable this script from script manager (included in the default installation of darktable. Thus no additional manual download required) and point it to the faces folder from the previous step.

## Technical process

1. Selected images are exported into a temporary location with a lowered resolution
2. The external tool is invoced with the photo and the path to the face folder as parameters
3. The result is parsed an dapplied as tags

## Usage

* start the recognition from the corresponding module ("face recognition") on the right side in the library view

## Source

https://github.com/darktable-org/lua-scripts/blob/master/contrib/face_recognition.lua

## Limitations


## Author

Sebastian Witt

## Change Log
