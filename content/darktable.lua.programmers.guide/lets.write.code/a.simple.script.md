---
title: a simple script
id: a simple script
weight: 20
draft: false
author: "people"
---

Let's start with a simple script that displays a message on the darktable window.

Create a file, simple_script.lua, and enter the following:
```lua
local dt = require "darktable"
dt.print("A simple script writes to the screen")
```
then save the file.

Start darktable, then open script_manager and change the group to development. Press the power 
button next to `simple_script` to start it.

The message displays on the window.

Congratulations, you've written your first script.  Now let's talk about what it is doing line by line.

`local dt = require "darktable"` loads the darktable Lua library that has all the Application Programming Interface code that lets Lua talk to darktable.  `dt` is declared as a local variable which means it only exists in this script.

`dt.print("A simple script writes to the screen")` uses the darktable [print](../../../lua.api.manual/darktable/darktable.print.md) function to display the image on the screen.

If you leave the script running when you close darktable, the script will automatically start the next time you start darktable and the message will appear again.

But, you want to show off your script when you want, not just at startup.  So, how do we do that?

