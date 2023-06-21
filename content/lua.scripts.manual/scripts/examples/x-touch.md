---
title: x-touch
id: x-touch
weight: 120
draft: false
author: "people"
---

## Name

x-touch.lua - use an X-Touch Mini controller with darktable

## Description

This script will create virtual sliders that are mapped dynamically to
the most relevant sliders for the currently focused processing module.
Tailored modules are color zones, tone equalizer, color calibration and
mask manager properties. The script can easily be amended for other
devices or personal preferences. Virtual "toggle" buttons can be created
as well, that dynamically change meaning depending on current status.

## Usage

* require this script from your luarc file or start it from script_manager
* restart darktable if using the luarc file
* create shortcuts for each of the encoders on the x-touch mini
  to a virtual slider under lua/x-touch
  or import the following shortcutsrc file in the shortcuts dialog/preferences tab:

```
None;midi:CC1=lua/x-touch/knob 1
None;midi:CC2=lua/x-touch/knob 2
None;midi:CC3=lua/x-touch/knob 3
None;midi:CC4=lua/x-touch/knob 4
None;midi:CC5=lua/x-touch/knob 5
None;midi:CC6=lua/x-touch/knob 6
None;midi:CC7=lua/x-touch/knob 7
None;midi:CC8=lua/x-touch/knob 8
midi:E0=global/modifiers
midi:F0=global/modifiers;ctrl
midi:F#0=global/modifiers;alt
midi:G#-1=iop/blend/tools/show and edit mask elements
midi:A-1=iop/colorzones;focus
midi:A#-1=iop/toneequal;focus
midi:B-1=iop/colorbalancergb;focus
midi:C0=iop/channelmixerrgb;focus
```

## Additional Software Required


## Limitations


## Author

Diederik ter Rahe

## Change Log
