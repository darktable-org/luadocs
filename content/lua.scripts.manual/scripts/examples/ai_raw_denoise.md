---
title: ai_raw_denoise
id: ai_raw_denoise
weight: 6
draft: false
author: "people"
---

## Name

ai_raw_denoise.lua - example script demonstrating the darktable.ai Lua
API by denoising the selected raw images with tile-based inference
on the raw CFA.

## Description

Adds an "AI raw denoise" panel to the lighttable right column with
a "denoise selected" button. Each selected image's raw CFA is
loaded, Bayer-packed to 4 channels, run tile-by-tile through the
currently enabled rawdenoise model (which denoises AND demosaicks
in one pass), and saved as a LinearRaw DNG grouped with the
source image.

Demonstrates:
* model lookup via dt.ai.model_for_task
* loading model variant files via dt.ai.load_model file arg
* raw CFA loading via dt.ai.load_raw
* tensor bayer_pack for 4-channel CFA tiling
* tile loop with non-trivial input->output scale (here 1 -> 2)
* edge-replicated padding to suppress border artifacts
* LinearRaw DNG output via dt.ai.save_dng_linear
* background job with progress bar and cancellation

## Usage

* start this script from script_manager or require it in the user luarc
* select one or more raw images in lighttable
* click the "denoise selected" button in the AI raw denoise panel

## Additional Software Required

* a rawdenoise model enabled in preferences -> AI
(e.g. rawdenoise-nind)

## Limitations

* Bayer sensors only. The script loads model_bayer.onnx and uses
bayer_pack, which assumes a 2x2 Bayer layout. X-Trans and
Foveon sensors need model_linear.onnx with a different
preprocessing pipeline (no bayer_pack, demosaicked input).
* Image must be at least TILE_SIZE x TILE_SIZE in packed pixels
(1024 x 1024 of CFA for the default 512 packed tile size).
* If a save fails mid-batch the Lua error propagates and aborts
the whole job. Wrap denoise_one in pcall if you need
batch-robust behaviour.

## Author

Andrii Ryzhkov

## Change Log
