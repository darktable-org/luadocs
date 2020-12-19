---
title: passport_guide
id: passport_guide
weight: 230
draft: false
author: "people"
---

## Name


## Description

guides for cropping passport photos based on documents from the Finnish police
(https://www.poliisi.fi/instancedata/prime_product_julkaisu/intermin/embeds/poliisiwwwstructure/38462_Passikuvaohje_EN.pdf) describing passport photo dimensions of 47x36 mm and 500x653 px for digital biometric data stored in passports. They use ISO 19794-5 standard based on ICAO 9303 regulations which should also be compliant for all of Europe.

## Usage

* add the following line in the file $CONFIGDIR/luarc
  require "passport_guide"
* (optional) add the line:
  "plugins/darkroom/clipping/extra_aspect_ratios/passport 36x47mm=47:36"
  to $CONFIGDIR/darktablerc
* when using the cropping tool, select "passport" as guide and if you added the line in your luarc
  select "passport 36x47mm" as aspect

## Additional Software Required


## Limitations


## Author

Kåre Hampf
