---
title: website_gallery_export
id: website_gallery_export
weight: 340
draft: false
author: "people"
---

## Name

website_gallery_export

## Description

This new gallery export modules replaces the old website gallery export. It consists of a gallery view of all images and a modal view that shows a single image, either in the browser window or in fullscreen (not supported for iOS devices).

In modal view, the user can switch to the previous and next image using mouse controls, keyboard shortcuts or swipe gestures when using a touchscreen.

Tapping/clicking on the image switches to a zoomed mode (1:1 view) or back to the full image view.

Keyboard shortcuts:

space/arrow right: next photo
backspace/arrow left: previous photo
escape: back to gallery view or exit from fullscreen view

## Usage

After enabling the module in the script manager (contrib section), you can chose "website gallery (new)" as target storage in the export module.

This setting will create an HTML gallery from all selected images.

You can provide a title for the gallery. The destination directory will contain all necessary files for the gallery. You can view it locally by opening the embedded index.html in a web browser or copy it to a webserver.


## Additional Software Required

If available, exiftool will be used to get the exact dimensions of the exported photos. Otherwise the image frame in the gallery view might be off for some pixels.

## Limitation
The formats for the exported image are currently limited to JPEG, PNG, WebP and TIFF.

Currently there is no access control. Be careful when making the gallery accessible via a web server if the images contains any individuals who did not give permission to publish these photos.

## Author

Tino Mettler

## Change Log
