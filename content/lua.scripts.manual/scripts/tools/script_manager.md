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

* start/stop scripts - 
  * The top part of the window has the **category selector**.  The category corresponds to the directory that the scripts are in. Currently the categories are _contrib_ for community contributed scripts, _examples_ for example scripts, _official_ for developer contributed scripts,
and _tools_ containing tools for managing the lua scripts.
  * The lower part of the window contains the paged interface for the scripts contained in the selected category.  There are arrow buttons for navigating the pages and an indicator showing what the current page is and how many pages of scripts there are for the current category.    The number of buttons defaults to 10, but is configurable anywhere between 5 and 20 depending on how much screen real estate you want to use.  The scripts are sorted alphabetically.  The button shows the name of the script and it's current status, started or stopped.  Clicking the script button toggles the script from started to stopped and back again.

* configure - this window allows changing the number of buttons used to display scripts.  Move the slider to select the number of buttons, click the _change number of buttons_  button and the number of buttons will change and the action will change back to the start/stop scripts window.

* install/update scripts - This window allows installing additional script repositories and updating installed repositories.
  * update - select the scripts to update from the _scripts to update_ dropdown.  Click the _update scripts_ button to do the update.
  * install - additional script repositories can be added to your lua scripts.  To add another repository fill in the _URL to download additional scripts from_ and then fill in the _new category to place scripts in_. Click the _install additional scripts_ button and the category \(directory\) is created and a git clone is performed to retrieve the git repository.  EXAMPLE: fill in _URL to download additional scripts from_ with https://github.com/wpferguson/extra-dt-lua-scripts.git and the _new category to place scripts in_ with wpferguson.  Click the button to install the scripts.  The scripts are retrieved and added to the user interface and the window changes to the newly installed script category.

  * disable scripts - the lua scripts are installed by the darktable scripts installer.  If you install them and later decide you no longer want them cluttering up your user interface, this option can disable them and stop them from starting.  Once they are disabled, the way to enable them again is to rename a file using the terminal and command line.  To disable the scritps first click the checkbox to enable the _Disable Scripts_ button.  This is to prevent accidentally disabling the lua scripts.  Once the _Disable Scripts_ button is active, click it to disable the scripts.  When the button is clicked, the luarc file is renamed to luarc.disabled which results in the scripts not starting the next time darktable starts.


## Additional Software Required

git - [git-scm.com](https://git-scm.com/) - git is used to install and update the scripts.  script_manager will still run if git is not installed or accessible, but installing and updating scripts will not be possible.


## Limitations

* There isn't currently a way to stop an executing script and remove it from the interface, so when a script is stopped the script preference is set to not start the next time darktable starts.

* If the scripts are disabled by choice the only way to enable them is by renaming the file luarc.disabled to luarc.  Then file is located in the user's darktable configuration directory, $HOME/.config/darktable on linux and macos and %LOCALAPPDATA%\\darktable on windows.

## Author

Bill Ferguson \<wpferguson@gmail.com\>

## Change Log

20201225 - Rewrite for darktable 3.4 - Merry Christmas
