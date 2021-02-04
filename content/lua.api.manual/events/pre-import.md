---
title: pre-import
id: pre-import
weight: 90
draft: false
author: "people"
---

`event`

This event is trigger before any import action

# pre-import.callback

```
function(
  event : string,
  images : table of string
)
```

* **event** - _string_ - The name of the event that triggered the callback.
* **images** - _table of string_ - The files that will be imported. Modifying this table will change the list of files that
will be imported.

# pre-import.extra registration parameters

This event has no extra registration parameters.
