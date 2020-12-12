---
title: image_stack
id: image_stack
weight: 180
draft: false
author: "people"
---

## Name

image_stack.lua - process a stack of images

## Description

This script provides another storage (export target) for darktable.  Selected
images are exported in the specified format to temporary storage.  The images are aligned
if the user requests it. When the images are ready, imagemagick is launched and uses
the selected evaluate-sequence operator to process the images.  The output file is written
to a filename representing the imput files in the format specified by the user.  The resulting 
image is imported into the film roll.  The source images can be tagged as part of the file 
creation so that  a user can later find the contributing images.

## Usage

* require this script from your main lua file
* select the images to process with image_stack
* in the export dialog select "image stack" and select the format and bit depth for the
  exported image
* Select whether the images need to be aligned.
* Select the stack operator
* Select the output format
* Select whether to tag the source images used to create the resulting file
* Specify executable locations if necessary
* Press "export"
* The resulting image will be imported

## Additional Software Required

* align_image_stack - http://www.hugin.org
* imagemagick - http://www.imagemagick.org

## Limitations

Mean is a fairly quick operation.  On my machine (i7-6800K, 16G) it takes a few seconds.  Median, on the other hand
takes approximately 10x longer to complete.  Processing 10 and 12 image stacks took over a minute.  I didn't test all
the other functions, but the ones I did fell between Mean and Median performance wise.

## Author

Bill Ferguson - wpferguson@gmail.com

## See Also 

* Thanks to Pat David and his blog entry on blending images, https://patdavid.net/2013/05/noise-removal-in-photos-with-median_6.html
