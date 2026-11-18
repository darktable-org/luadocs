---
title: script_manager
id: script_manager
weight: 50
draft: false
author: "people"
---

## Name

script_manager.lua - a tool for managing the darktable lua scripts

## Description

script_manager is designed to be called from the users luarc file and used to manage the lua scripts.

On startup script_manager scans the lua scripts directory to see what scripts are present.
Scripts are sorted by 'category' based on what sub-directory they are in.  With no 
additional script repositories iinstalled, the categories are contrib, examples, official
and tools.  When a category is selected the buttons show the script name and whether the
script is started or stopped.  The button is a toggle, so if the script is stopped click 
the button to start it and vice versa.

## Features

* the number of script buttons shown can be changed to any number between 5 and 20.  The default is 10 buttons.  This can be changed in the configuration action.

* additional repositories of scripts may be installed from the install/update action.

* installed scripts can be updated from the install/update action.  This includes extra repositories that have been installed.

* the lua scripts can be disabled if desired from the install/update action.  

* script_manager is automatically installed and enabled when the lua scripts are installed by the darktable scripts_installer.

## Usage

Usage instructions are available in [darktables user manual](https://docs.darktable.org/usermanual/5.6/en/module-reference/utility-modules/lighttable/scripts/).

## Additional Software Required

git - [git-scm.com](https://git-scm.com/) - git is used to install and update the scripts in darktable versions < 5.6.  script_manager will still run if git is not installed or accessible, but installing and updating scripts will not be possible.

## Author

Bill Ferguson \<wpferguson@gmail.com\>

## Change Log

20201225 - Rewrite for darktable 3.4 - Merry Christmas
20261117 - update to current status
