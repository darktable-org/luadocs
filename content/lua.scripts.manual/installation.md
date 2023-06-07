---
title: installation
id: installation
weight: 20
draft: false
author: "people"
---

## Download and Install

The recommended method of installation is using git to clone the repository. This ensures that all dependencies on other scripts
are met as well as providing an easy update path.

### snap packages

The snap version of darktable comes with lua included starting with version 2.4.3snap2.

Ensure git is installed on your system. If it isn't, use the package manager to install it. Then open a terminal and:

    cd ~/snap/darktable/current
    git clone https://github.com/darktable-org/lua-scripts.git lua

### flatpak packages

Flatpak packages now use the internal lua interpreter.


Ensure git is installed on your system. If it isn't, use the package manager to install it. Then open a terminal and:

    cd ~/.var/app/org.darktable.Darktable/config/darktable
    git clone https://github.com/darktable-org/lua-scripts.git lua

### appimage packages

These packages run in their own environment and don't have access to a lua interpreter, therefore the scripts can't run. The packagers could enable the internal interpreter, or allow the package to link the interpreter from the operating system, or bundle a copy of lua with the package. If you use one of these packages and wish to use the lua scripts, please contact the package maintainer and suggest the above fixes.

### Linux and MacOS

Ensure git is installed on your system. If it isn't, use the package manager to install it. Then open a terminal and:

    cd ~/.config/darktable/
    git clone https://github.com/darktable-org/lua-scripts.git lua

### Windows

Ensure git is installed on your system. Git can be obtained from https://gitforwindows.org/, as well as other places. If you use the gitforwindows.org distribution, install the Git Bash Shell also as it will aid in debugging the scripts if necessary. Then open a command prompt and run:

    cd %LOCALAPPDATA%\darktable
    git clone https://github.com/darktable-org/lua-scripts.git lua

If you don't have %LOCALAPPDATA%\darktable you have to start dartable at least once, because the directory is created at the first start of darktable.

## Enabling

When darktable starts it looks for a file name `~/.config/darktable/luarc` (`%LOCALAPPDATA%\darktable\luarc` for windows) and reads it to see which scripts to include. The file is a plain text file with entries of the form `require "<directory>/<name>"` where directory is the directory containing the scripts, from the above list, and name is the name from the above list. To include GIMP the line would be `require "contrib/gimp"`.

The recommended way to enable and disable specific scripts is using the script manager module.  To use script manager do the following:

### Linux or MacOS

    echo 'require "tools/script_manager"' > ~/.config/darktable/luarc

### Windows ( via command prompt )

    echo require 'tools/script_manager' > %LOCALAPPDATA%\darktable\luarc

### Snap

    echo 'require "tools/script_manager"' > ~/snap/darktable/current/luarc

### Flatpak

    echo require "tools/script_manager"' > ~/.var/app/org.darktable.Darktable/config/darktable/luarc

You can also create or add lines to the luarc file from the command line:

`echo 'require "contrib/gimp"' > ~/.config/darktable/luarc` to create the file with a gimp entry\
or `echo 'require "contrib/hugin"' >> ~/.config/darktable/luarc` to add an entry for hugin.

On windows from a command prompt:

`echo require "contrib/gimp" > %LOCALAPPDATA%\darktable\luarc` to create the file with a gimp entry\
or `echo require "contrib/hugin" >> %LOCALAPPDATA%\darktable\luarc` to add an entry for hugin.

## Disabling

To disable a script open the luarc file in your text editor and insert `--` at the start of the line containing the script you wish to disable, then save the file.

## Updating

To update the script repository, open a terminal or command prompt and do the following:

### Snap

    cd ~/snap/darktable/current/lua
    git pull


### Flatpak

    cd ~/.var/app/org.darktable.Darktable/config/darktable/lua
    git pull

### Linux and MacOS

    cd ~/.config/darktable/lua/
    git pull

### Windows

    cd %LOCALAPPDATA%\darktable\lua
    git pull
