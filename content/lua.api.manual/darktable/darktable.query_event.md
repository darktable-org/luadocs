---
title: darktable.query_event
id: darktable.query_event
weight: 196
draft: false
author: "people"
---

```
function(
  event_name : string,
  event_type : string,
) : boolean
```

This function determines if an event is registered by [darktable.register_event](darktable.register_event.md).
Events are documented in the [event](../events) section.

* **event_name** - _string_ - The name of the event registered. The combination of event_name and event_type must be unique.
* **event_type** - _string_ - The type of the event registered.
* **return** - _boolean_ - True if the event exists, otherwise false
