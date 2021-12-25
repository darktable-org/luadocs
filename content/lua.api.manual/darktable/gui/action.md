---
title: darktable.gui.action
id: action
weight: 15
draft: false
author: "people"
---

```
function(
  path : string,
  instance : integer,
  element : string,
  effect : string,
  speed : integer
) : string
```

Will perform the specified effect on the path, instance, and element of an action, or return the status.

* **path** - _string_ - The full path of an action, i.e. \'lib/filter/view\'.
* **instance** - integer - The instance of an image processing module to execute action on".
* **element** - _string_ - The element of an action, for example 'selection', or leave empty for default".
* **effect** - _string_ - The effect of an action, for example 'next', or leave empty for default".
* **speed** - integer - 1 causes the effect to be performed, 0 or NaN returns the current status.
* **return** - _string_ - The current status of the action.
