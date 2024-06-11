---
title: passport_guide_germany
id: passport_guide_germany
weight: 231
draft: false
author: "people"
---

## Name

passport_guide_germany

## Description

Guides for cropping passport and ID card ("Personalausweis") photos based on the "Passbild-Schablone" 
from the German Federal Ministry of the Interior and Community. 
(https://www.bmi.bund.de/SharedDocs/downloads/DE/veroeffentlichungen/themen/moderne-verwaltung/ausweise/passbild-schablone-erwachsene.pdf?__blob=publicationFile&v=3) 

## Usage

* Start script from script_manager
* (optional) add the line:
  "plugins/darkroom/clipping/extra_aspect_ratios/passport 35x45mm=45:35" 
  to $CONFIGDIR/darktablerc
* when using the cropping tool, select "Passport Photo Germany" as guide and if you added the aspect ratio line 
in your darktablerc file then
select "passport 35x45mm" as aspect

## Additional Software Required


## Limitations


## Author

Christian Sültrop

## Change Log
