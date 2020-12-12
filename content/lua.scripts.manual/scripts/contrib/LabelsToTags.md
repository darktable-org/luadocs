---
title: LabelsToTags
id: LabelsToTags
weight: 210
draft: false
author: "people"
---

## Name

LabelsToTags.lua - mass apply tags to images
## Description

Allows the mass-application of tags using color labels and ratings
as a guide.

## Usage

In your 'luarc' file or elsewhere, use the function
'register_tag_mapping', defined in this module, to specify
one or more tag mappings for use by the module.
Any mappings so registered will be selectable, according
to their given names, in the module's "mapping" combo box.

A mapping takes the form of a table mapping patterns to
lists of tags. A pattern consists of 6 characters, of which
the first five represent color labels and the last the rating.
Each color label character may be '+', '-', or '*',
indicating that for this pattern to match, the corresponding
color label, respectively, must be on, must be off, or can be
either. Similarly, the rating character may be a numeral
between 0 and 5, "R" for rejected, or "*" for "any value."

An example call to 'register_tag_mapping' is provided in a
comment at the end of this file.

When the "Start" button is pressed, the module will
iterate over each selected image and check the state of
that image's color labels and rating against each pattern
defined in the selected mapping. For each pattern that
matches, the corresponding tags will be added to the
image. Any such tag not already existing in the database
will be created.

## Additional Software Required


## Limitations


## Author

August Schwerdfeger - august@schwerdfeger.name
