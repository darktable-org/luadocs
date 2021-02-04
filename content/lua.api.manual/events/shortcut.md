---
title: shortcut
id: shortcut
weight: 110
draft: false
author: "people"
---
`event`

This event registers a new keyboard shortcut. The shortcut isn't bound to any key until
the users does so in the preference panel. The event is triggered whenever the shortcut
is triggered. This event can only be registered once per value of shortcut.

# shortcut.callback

```
function(
  event : string,
  shortcut : string
)
```

* **event** - _string_ - The name of the event that triggered the callback.
* **shortcut** - _string_ - The tooltip string that was given at registration time.

# shortcut.extra registration parameters
* **tooltip** - _string_ - The string that will be displayed on the shortcut preference panel describing the
shortcut.

