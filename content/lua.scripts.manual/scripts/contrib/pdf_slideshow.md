---
title: pdf_slideshow
id: pdf_slideshow
weight: 240
draft: false
author: "people"
---

## Name

pdf_slideshow.lua - generate a pdf slideshow

## Description

Generates a PDF slideshow (via Latex) containing all selected images
one per slide.

## Usage

* start this script from script manager

This plugin will add a new exporter that will allow you to generate a pdf slideshow.
The interface will let you add:
   - a global title for the slideshow (prefix in all slide label)
   - a delay for the transition between each slide

Each slide will contain a single picture with a label at the bottom with the
format (all fields can be the empty string):

   \<global title\> / \<image creator\> / \<image title\>

## Additional Software Required

* a PDF-Viewer
* pdflatex (Latex)

## Limitations


## Author

Pascal Obry
