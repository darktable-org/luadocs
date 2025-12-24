---
title: collection-changed
id: collection-changed
weight: 11
draft: false
author: "people"
---

`event`

This event is triggered whenever the lighttable collection changes.  The event triggers anytime the collection module rules change, including simply adding a rule, so the user needs to check to ensure there is actually a change by keeping track of the number of images or checking the collection rules.

# collection-changed.callback

```
function(
  event : string,
)
```

* **event** - _string_ - The name of the event that triggered the callback.

# collection-changed.extra registration parameters

This event has no extra registration parameters.
