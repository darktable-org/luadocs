---
title: darktable.gui.libs overview
id: overview
weight: 10
draft: false
author: "people"
---

This table allows referencing all lib objects.
lib objects are the graphical blocks within each view.
To quickly figure out which lib is which, you can use the following code, which will make a
given lib blink.

```
local dt = require "darktable"
local tested_module="global_toolbox"
dt.gui.libs[tested_module].visible=false
dt.control.sleep(2000)
while true do
  dt.gui.libs[tested_module].visible = not dt.gui.libs[tested_module].visible
  dt.control.sleep(2000)
end
```
