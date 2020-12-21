---
title: darktable.register_event
id: darktable.register_event
weight: 50
draft: false
author: "people"
---

```
function(
  event_type : string,
  callback : function,
  ... : variable
)
```

This function registers a callback to be called when a given event happens.
Events are documented in the [event](../events) section.

* **event_type** - _string_ - The name of the event to register to.
* **callback** - _function_ - The function to call on event. The signature of the function depends on the type of
event.
* **...** - _variable_ - Some events need extra parameters at registration time; these must be specified here.
