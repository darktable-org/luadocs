---
title: OpenInExplorer
id: OpenInExplorer
weight: 220
draft: false
author: "people"
---

## Name

OpenInExplorer.lua - open an images containing folder

## Description

This plugin adds the module "OpenInExplorer" to darktable's lighttable view.

## Usage

Require this file in your luarc file, as with any other dt plug-in

Select the photo(s) you wish to find in your operating system's file manager and press "show in file explorer" in the "selected images" section.

- Nautilus (Linux), Explorer (Windows), and Finder (macOS prior to Mojave) will open one window for each selected image at the file's location. The file name will be highlighted.

- On macOS Mojave and Catalina the Finder will open one window for each different directory. In these windows only the last one of the corresponding files will be highlighted (bug or feature?).

- Dolphin (Linux) will open one window with tabs for the different directories. All the selected images' file names are highlighted in their respective directories.

As an alternative option you can choose to show the image file names as symbolic links in an arbitrary directory. Go to preferences|Lua options. This option is not available for Windows users as on Windows solely admins are allowed to create links.

- Pros: You do not clutter up your display with multiple windows. So there is no need to limit the number of selections.

- Cons: If you want to work with the files you are one step behind the original data.


## Additional Software Required


## Limitations


## Author

Kevin Ertel  
Volker Lenhardt  
Bill Ferguson

