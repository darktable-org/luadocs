---
title: ai_denoise
id: ai_denoise
weight: 3
draft: false
author: "people"
---

## Name

ai_denoise.lua - example script demonstrating the darktable.ai Lua API by denoising the selected images with tile-based inference.

## Description

Adds an "AI denoise" module to the lighttable right column with a
"denoise selected" button. Each selected image is loaded through
the develop pipeline (so denoise sees the output of all enabled
IOPs, not the original raw), run tile-by-tile through the active
denoise model, and saved as a 16-bit TIFF grouped with the source.

Demonstrates:
* model lookup via dt.ai.model_for_task
* tensor crop/paste for tile-based inference
* linear <-> sRGB conversion (NR models train on gamma input)
* edge-replicated padding to suppress border artifacts
* background job with progress bar and cancellation

## Usage

* start this script from script_manager or require this script in in the user luarc
* select one or more images in lighttable
* click the "denoise selected" button in the AI denoise module

## Additional Software Required

* a denoise model enabled in preferences -> AI (denoise-nind,
denoise-nafnet, ...)

## Limitations

* Image must be at least TILE_SIZE x TILE_SIZE (768 x 768 for denoise-nind / denoise-nafnet); smaller inputs return an error.
* If a save fails mid-batch the Lua error propagates and aborts the whole job. Wrap denoise_one in pcall if you need
batch-robust behaviour.

## Author

Andrii Ryzhkov

## Change Log
