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

script_manager is designed to run as a standalone script so that it
may be used as a drop in luarc file in the user's $HOME/.config/darktable
($HOME/AppData/Local/darktable on windows)  directory.  It may also be 
required from a luarc file.

On startup script_manager checks to see if there is an  existing scripts directory.  
If there is an existing lua scripts directory then it is read to see what scripts are present.  
Scripts are sorted by "category" based on what subdirectory they are found in, thus with a lua 
scripts directory that matched the current repository the categories would be contrib, examples, 
offical, and tools.  Each script has an Enable/Disable button to enable or disable the script.

A link is created to the user's Downloads directory on linux, unix and MacOS.  Windows users must create the 
link manually using mklink.exe.  Additional "un-official" scripts may be downloaded 
from other sources and placed in the users Downloads directory.  These scripts all fall in a downloads category.  
They also each have an Enable/Disable button.


## Usage


## Additional Software Required


## Limitations


## Author


## Change Log
