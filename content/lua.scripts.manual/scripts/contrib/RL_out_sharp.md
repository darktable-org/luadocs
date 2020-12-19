---
title: RL_out_sharp
id: RL_out_sharp
weight: 290
draft: false
author: "people"
---

## Name

RL_out_sharp.lua - Richardson-Lucy output sharpening using GMic

## Description

This script provides a new target storage "RL output sharpen". 
Images exported will be sharpened using GMic (RL deblur algorithm)

### EXAMPLE

set sigma = 0.7, iterations = 10, jpeg output quality = 95,
to correct blur due to image resize for web usage

## Usage

* start this script from script manager
* in lua preferences, select the GMic cli executable
* from "export selected", choose "RL output sharpen"
* configure output folder 
* configure RL parameters with sliders
* configure temp files format and quality, jpg 8bpp (good quality) 
  and tif 16bpp (best quality) are supported
* configure other export options (size, etc.)
* export, images will be first exported in the temp format, then sharpened
* sharpened images will be stored in jpg format in the output folder

## Additional Software Required

GMic command line interface (CLI) https://gmic.eu/download.shtml

## Limitations

MAC compatibility not tested
Although Darktable can handle file names containing spaces, GMic cli cannot, 
  so if you want to use this script please make sure that your images do not
  have spaces in the file name and path

## Author

Marco Carrarini - marco.carrarini@gmail.com
