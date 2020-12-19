---
title: HDRMerge
id: name
weight: 160
draft: false
author: "people"
---

## Name

HDRMerge.lua - create an HDR image using HDRMerge
## Description

This plugin adds the module 'HDRMerge' to darktable's lighttable view

## Usage

Start this script using script manager.

On the initial startup go to darktable settings > lua options and set your executable paths and other preferences, then restart darktable

Select bracketed images and press the Run HDRMerge button. The resulting DNG will be auto-imported into darktable.
Additional tags or style can be applied on auto import as well, if you desire.

### Base Options

Select your desired BPS (bits per sample and Embedded Preview Size. 

### Batch Options

Select if you want to run in batch mode or not
Select the gap, in seconds, between images for auto grouping in batch mode

See HDRMerge manual for further detail: http://jcelaya.github.io/hdrmerge/documentation/2014/07/11/user-manual.html

### Auto-import Options

Select a style, whether you want tags to be copied from the original, and any additional tags you desire added when the new image is auto-imported

## Additional Software Required

HDRMerge ver. 4.5 or greater

## Limitations


## Author

Kevin Ertel
