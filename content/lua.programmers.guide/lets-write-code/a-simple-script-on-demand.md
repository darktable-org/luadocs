---
title: a simple script on demand
id: a-simple-script-on-demand
weight: 20
draft: false
author: "people"
---

We want to display the message from [a simple script](a-simple-script.md) when we want, not just when darktable starts or when we first start the script.

So, how do we do that?

Lua scripts are event driven.  The event driving a_simple_script.lua is script_manager starting the script.  When the event occurs, the script runs until then end and then it's finished.

So what we need is an event to drive the script to display the message on demand.  The event we need is a [shortcut](../../lua.api.manual/events/shortcut.md) that allows the user to assign a keyboard sequence to trigger the event.

In the development directory, copy simple_script.lua to simple_script_on_demand.lua and open it in an editor.  We are going to wrap the `dt.print` command in the shortcut event.  Change simple_script_on_demand.lua to look like the following:

```lua
local dt = require "darktable"
dt.register_event("simple_script_on_demand", "shortcut",
  function(event, shortcut)
    dt.print("A simple script writes to the screen on demand")
  end, 
  "write simple script message to the screen"
)
```

Restart darktable and open script_manager in the development category.  simple_script_on_demand should appear in the list of scripts.  Start it and notice no message appears on the screen.

Go the the preferences, then shortcuts, then Lua scripts.  Double click on the `write simple script message to the screen` line and assign a key sequence to it.  Close the preferences, then hit the key sequence and see the message appear on screen.  Hit it again and the message appears again.
