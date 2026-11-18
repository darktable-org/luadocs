---
title: a simple script
id: a-simple-script
weight: 10
draft: false
author: "people"
---

Let's start with a simple script and build it up, step by step, until it displays a message on the darktable window.

Create a file, `simple_script.lua`, and enter a single line of standard Lua:
```lua
print("Hello World !")
```
then save the file.

To run it, start darktable, open script_manager and change the group to development. Press the power button next to `simple_script` to start it. If you started darktable from a console, you will see `Hello World !` printed there. Nothing fancy, but it's a start.

At this point there is nothing darktable-specific in the script — we simply use Lua's standard `print` function to print a string. To do more than that, the script needs to talk to darktable.

## talking to darktable

To access the darktable API you first need to `require` it and save the returned object in a variable. Change `simple_script.lua` to look like this:
```lua
local dt = require "darktable"
dt.print("A simple script writes to the screen")
```
Restart the script from script_manager, and this time the message displays on the darktable window.

Congratulations, you've written your first script. Now let's talk about what it is doing line by line.

`local dt = require "darktable"` loads the darktable Lua library that has all the Application Programming Interface code that lets Lua talk to darktable. `dt` is declared as a local variable, which means it only exists in this script.

`dt.print("A simple script writes to the screen")` uses the darktable [print](../../lua.api.manual/darktable/darktable.print.md) function to display the message on the screen.

## printing traces to the console

`dt.print` shows a message on the window. For debugging you often want output on the console instead. darktable provides [print_error](../../lua.api.manual/darktable/darktable.print_error.md) for that:
```lua
dt.print_error("Hello World !")
```
Run this and ... nothing happens. `dt.print_error` is just like Lua's `print`, but it only prints its message if you have enabled Lua traces by running darktable with `darktable -d lua` on the command line. This is the recommended way to produce trace output in a darktable Lua script.

## what next

If you leave the script running when you close darktable, it will automatically start the next time you start darktable and the message will appear again.

But you want to show off your script when *you* want, not just at startup. So how do we do that? That is the subject of [a simple script on demand](a-simple-script-on-demand.md).

Scripts can also be loaded through a `luarc` file instead of script_manager. See [how darktable loads scripts](../scripts-loading.md) for the details.
