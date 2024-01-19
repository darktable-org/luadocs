---
title: darktable.gui.mimic
id: action
weight: 60
draft: false
author: "people"
---

```
function(
  widget_type : string,
  name : string,
  callback : function
)
```

Provides a virtual widget that can be assigned to a shortcut.

* **widget_type** - _string_ - The type of widget to mimic, one of: button, slider, dropdown.
* **name** - _string_ - The name of the virtual widget that a shortcut can be assigned to.
* **callback** - _function_ - A function containing [darktable.gui.action](../gui/action.md) calls to execute.

## Example

```
local dt = require "darktable"

dt.gui.mimic("slider", "multi-contrast",
  function(action, element, effect, size)
      if dt.gui.action("iop/filmicrgb", "focus") == 1 then
        which = "iop/filmicrgb/contrast"
      else
        which = "iop/colorbalancergb/contrast"
      end
      return dt.gui.action(which, element, effect, size)
    end
)
```