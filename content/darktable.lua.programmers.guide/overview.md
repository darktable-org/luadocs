---
title: overview
id: overview
weight: 10
---

[Lua](http://www.lua.org/) is an independent project founded in 1993, providing a powerful, fast, lightweight, embeddable scripting language. Lua is widely used by many open source applications, in commercial programs, and for games programming. 

darktable uses Lua version 5.4. 

Describing the principles and syntax of Lua is beyond the scope of this manual. For a detailed introduction see the [Lua reference manual](http://www.lua.org/manual/5.4/manual.html).

darktable has the Lua scripting language embedded in the darktable executable.  Embedding the language gives Lua access to the darktable internals, allowing it manipulate image information, metadata, and the darktable UI.  Using Lua, images can be imported, exported, and sent to external executables for further processing.

Lua is the tool for implementing user custom workflows, responding to darktable events to take user specified actions.  Lua scripts can be used to define actions for darktable to perform when an event is triggered. One example might be calling an external application during file export in order to apply additional processing steps outside of darktable.

darktable comes with a number of [scripts included](darktables-scripts.md). The central orchestrator for scripts is the script manager (see [basic principles](basic-principles.md)).
