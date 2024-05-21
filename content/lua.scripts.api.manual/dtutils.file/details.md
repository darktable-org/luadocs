---
title: details
id: details
weight: 10
draft: false
author: "people"
---

## NAME

details

## SYNOPSIS

common darktable lua file functions

## USAGE
```
local df = require "lib/dtutils.file"
```
## DESCRIPTION

The **dtutils.file** library provides common file manipulation functions used in
constructing darktable lua scripts

## RETURN VALUE

**df** - _library_ - the file functions

## FUNCTIONS

* [check_if_bin_exists](check_if_bin_exists.md) - check if an executable exists

* [check_if_file_exists](check_if_file_exists.md) - check if a file or path exist

* [chop_filetype](chop_filetype.md) - remove a filetype from a filename

* [create_unique_filename](create_unique_filename.md) - create a unique filename from the supplied argment

* [executable_path_widget](executable_path_widget.md) - create a widget to get executable path preferences

* [file_copy](file_copy.md) - copy a file to another name/location

* [file_move](file_move.md) - move a file from one directory to another

* [filename_increment](filename_increment.md) - add a two digit increment to a filename

* [get_basename](get_basename.md) - get the filename without the path or extension

* [get_executable_path_preference](get_executable_path_preference.md) - return the path to an executable from a preference

* [get_filename](get_filename.md) - get the filename and extension from a file path

* [get_filetype](get_filetype.md) - get the filetype from a filename

* [get_path](get_path.md) - get the path from a file path

* [mkdir](mkdir.md) - create the directory(ies) if they do not already exists

* [rmdir](rmdir.md) - recursively remove a directory

* [sanitize_filename](sanitize_filename.md) - make a filename safe to pass as an argument

* [set_executable_path_preference](set_executable_path_preference.md) - set a preference for the path to an executable

* [split_filepath](split_filepath.md) - split a filepath into parts

## LICENSE

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 3 of the License, or
(at your option) any later version.
This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.
You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

