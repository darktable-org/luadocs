---
title: terse_dump
id: terse-dump
weight: 40
draft: false
author: "people"
---

## NAME

terse_dump

## SYNOPSIS

set darktable.debug.known to shorten all image dumps to a single line

## USAGE
```
local dd = require "lib/dtutils.debug"
dd.terse_dump()
```
## DESCRIPTION

**terse_dump** sets **darktable.debug.known** to shorten all images to a single line.
If you don't need to debug the content of images, this will avoid them flooding your logs.
