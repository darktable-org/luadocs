---
title: overview
id: overview
weight: 10
---

[Lua](http://www.lua.org/) is an independent project founded in 1993, providing a powerful, fast, lightweight, embeddable scripting language. Lua is widely used by many open source applications, in commercial programs, and for games programming. darktable uses Lua version 5.4.

Describing the principles and syntax of Lua is beyond the scope of this manual. For a detailed introduction see the [Lua reference manual](http://www.lua.org/manual/5.4/manual.html).

darktable has the Lua scripting language embedded in the darktable executable. Embedding the language gives Lua access to the darktable internals, allowing it to manipulate image information, metadata, and the darktable UI. Using Lua, images can be imported, exported, and sent to external executables for further processing.

Lua is the tool for implementing custom user workflows, responding to darktable events to take user-specified actions. Lua scripts can be used to define actions for darktable to perform when an event is triggered. One example where a new Lua script might be useful would be calling an external application during file export in order to apply additional processing steps outside of darktable.

This guide provides an introduction to writing Lua scripts for darktable; the page [how darktable loads scripts](scripts-loading.md) explains where darktable looks for scripts and how the script manager loads them. If instead you want to install and use the scripts that ship with darktable, see the [Lua Scripts Manual](../lua.scripts.manual/_index.md). All data structures and functions are documented in the [Lua API](../lua.api.manual/_index.md) reference manual.
