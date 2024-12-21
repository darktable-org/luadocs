---
title: dt_imageio_module_format_data_jpegxl
id: dt_imageio_module_format_data_jpegxl
weight: 155
draft: false
author: "people"
---

`dt_type`

Type object describing parameters to export to jpegxl.

Attributes:

* [parent](../attributes#parent) : [types.dt_imageio_module_format_t](../types/dt_imageio_module_format_t)

# dt_imageio_module_format_data_jpegxl.bpp

`number`

The bits per pixel to use at export time (10, 12, 16, 32).

Attributes:

* [write](../attributes#write)

# dt_imageio_module_format_data_jpegxl.pixel_type

`number`

Type of format for pixels, 0 for integer or 1 for floating point.

Attributes:

* [write](../attributes#write)

# dt_imageio_module_format_data_jpegxl.quality

`number`

The quality to use at export time.

Attributes:

* [write](../attributes#write)

# dt_imageio_module_format_data_jpegxl.original

`number`

The color profile used by the encoder.

* 0 - permit internal XYB color space conversion for more efficient lossy compression
* 1 - ensure no conversion to keep original image color space (implied for lossless)

Attributes:

* [write](../attributes#write)

# dt_imageio_module_format_data_jpegxl.effort

`number`

Encoding effort.  The effort used to encode the image, higher efforts will have better results at the expense of longer encoding times.

Attributes:

* [write](../attributes#write)

# dt_imageio_module_format_data_jpegxl.tier

`number`

Decoding speed.  The preferred decoding speed with some sacrifice of quality.

Attributes:

* [write](../attributes#write)

