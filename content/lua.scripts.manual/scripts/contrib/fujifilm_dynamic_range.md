---
title: fujifilm_dynamic_range
id: fujifilm_dynamic_range
weight: 105
draft: false
author: "people"
---

## Name

fujifilm_dynamic_range.lua - adjust darktable exposure by Fujifilm raw exposure bias

## Description

Support for adjusting darktable exposure by Fujifilm raw exposure
bias. This corrects for a DR100/DR200/DR400 "dynamic range" setting.

Based upon fujifilm_ratings by Ben Mendis

The relevant tag is RawExposureBias \(0x9650\). This appears to
represent the shift in EV for the chosen DR setting \(whether manual or
automatic\). Note that even at 100DR \("standard"\) there is an EV shift:

100 DR -> -0.72 EV
200 DR -> -1.72 EV
400 DR -> -2.72 EV

The ideal would be to use exiv2 to read this tag, as this is the same
code which darktable import uses. Unfortunately, exiv2 as of v0.27.3
can't read this tag. As it is encoded as a 4-byte ratio of two signed
shorts -- a novel data type -- it will require some attention to fix
this.

There is an exiv2-readable DevelopmentDynamicRange tag which maps to
RawExposureBias as above.  DevelopmentDynamicRange is only present
when tag DynamicRangeSetting \(0x1402\) is Manual/Raw \(0x0001\). When it
is Auto \(0x0000\), the equivalent data is tag AutoDynamicRange
\(0x140b\). But exiv2 currently can't read that tag either.

Hence for now this code uses exiftool to read RawExposureBias, as a
more general solution. As exiftool is approx. 10x slower than exiv2
\(Perl vs. C++\), this may slow large imports.

These tags have been checked on a Fujifilm X100S and X100V. Other
cameras may behave in other ways.

## Usage

Start this script from script manager

## Additional Software Required

exiftool (https://www.sno.phy.queensu.ca/~phil/exiftool/)

## Limitations

## Author

Dan Torop <dant@pnym.net>

## Change Log
