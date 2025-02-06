---
title: ultrahdr
id: ultrahdr
weight: 325
draft: false
author: "people"
---

## Name

ultrahdr.lua - Generate [Ultra HDR](https://developer.android.com/media/platform/hdr-image-format) JPEG images from various combinations of source images.

## Description

The plugin generates Ultra HDR images that embed intents targetting both SDR and HDR displays in one JPEG file. UltraHDR images can be generated from the following sources (stacks):

 * SDR + gain map
 * SDR + HDR
 * SDR only
 * HDR only

The output images use PQ P3 RGB color profile for the HDR intent, and Display P3 RGB for the SDR intent.

## Usage

1. **Install the script**. Require this script from your luarc file or start it from script_manager, and configure paths for the required binaries if they are not on the path.

2. **Prepare the source image(s)**. Depending on the selected workflow, you will need a combination of the following versions of each photo (with the same pixel dimensions):

    * Standard dynamic-range (*SDR*) image
    * High-dynamic range (*HDR*) image, e.g. created using darktable's HDR merge workflows, or externally.
    * Single channel *gain map* (a map indicating how much to brighten each pixel, in the SDR image, to produce the target HDR). You can create it by e.g. duplicating the SDR image, converting it to monochrome, and using the *tone equalizer* module to increase the contrast.

    Tag all source HDR images with *hdr* tag, and gain map images with *gainmap* tag. This is so the plugin correctly recognizes the source images when merging.

3. **Select source image(s)** in lighttable. To generate a single Ultra HDR JPEG, simply select all its source images. To generate multiple Ultra HDR JPEGs, make sure that the source images for a given Ultra JPEG all have the same file path and file name (ignoring extension), as that's how the plugin recognizes spearate source image 'stacks'. You can use darktable's duplicate image function for that.

4. **Configure the export**. Review the export parameters in the *UltraHDR* module in lighttable. 
5. **Generate UltraHDR**. Click *generate UltraHDR* button. 

## Additional Software Required

* `ultrahdr_app` utility from [libultrahdr](https://github.com/google/libultrahdr). Obtain this by [building](https://github.com/google/libultrahdr/blob/main/docs/building.md) or installing the binary through [package managers](https://repology.org/project/libultrahdr/versions).
* `exiftool`
* `ffmpeg`

## Limitations

darktable is currently not able to properly display HDR content ([#17710](https://github.com/darktable-org/darktable/issues/17710)). For HDR source images, adjust exposure of the HDR images before generating Ultra HDRs. This usually means adding an exposure module with -5.6 EV correction to HDR image (it should appear as very dark in darktable UI). See [this thread](https://discuss.pixls.us/t/manual-creation-of-ultrahdr-images/45004/33) for details.

Due to that limitation, an expected rendition of UltraHDR images usually takes a few tries, and the output images need to be previewed in a HDR-capable display and application (e.g. a Chromium-based browser).

## Author

  Krzysztof Kotowicz

