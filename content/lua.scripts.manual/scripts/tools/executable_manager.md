---
title: executable_manager
id: executable_manager
weight: 10
draft: false
author: "people"
---

## Name

executable_manager.lua - a tool for managing external executables used by darktable lua scripts

## Description

executable_manager is a tool for managing the executable preferences stored in the darktablerc file.
On startup the darktablerc file is scanned and a widget is built for each executable path.  The user
can select the executable from a drop down list and then modify the settings as desired.

Any changes made using executable_manager won't be saved in the darktablerc file until darktable exits, but
the preference is updated when the change is made so scripts will pick up the changes without restarting
darktable.

## Usage

* start this script from script manager

## Additional Software Required

None

## Limitations


## Author

Bill Ferguson - wpferguson@gmail.com

## Change Log
