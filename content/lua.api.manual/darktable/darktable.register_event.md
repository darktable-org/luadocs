---
title: darktable.register_event
id: darktable.register_event
weight: 190
draft: false
author: "people"
---

```
function(
  event_name : string,
  event_type : string,
  callback : function,
  ... : variable
)
```

This function registers a callback to be called when a given event happens.
Events are documented in the [event](../events) section.

* **event_name** - _string_ - The name of the event used to manipulate the event. The combination of event_name and event_type must be unique. **API 6.2.1**
* **event_type** - _string_ - The name of the event to register to.
* **callback** - _function_ - The function to call on event. The signature of the function depends on the type of
event.
* **...** - _variable_ - Some events need extra parameters at registration time; these must be specified here.
