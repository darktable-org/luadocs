---
title: photils
id: photils
weight: 250
draft: false
author: "people"
---

## Name

photils.lua - auto tag images based on feature recognition

## Description

 A darktable plugin that tries to predict keywords based on the selected image.
 This plugin uses photils-cli to handle this task. Photils-cli is an application
 that passes the image through a neural network, classifies it, and extracts the
 suggested tags. Everything happens offline without the need that your data are
 sent over the internet.

## Usage

* start this script from script manager
* Select an image
* Press "get tags"
* Select the tags you want from a list of suggestions
* Press "Attach .. Tags" to add the selected tags to your image

## Additional Software Required

* photils-cli - https://github.com/scheckmedia/photils-cli at the moment only
  available for Linux and MacOS

## Limitations

## Website

[photils](https://github.com/scheckmedia/photils-dt)

## Author

Tobias Scheck
