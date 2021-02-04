---
title: darktable.destroy_event
id: darktable.destroy_event
weight: 195
draft: false
author: "people"
---

**API 6.2.1**

```
function(
  event_name : string,
  event_type : string,
)
```

This function removes the callback registered by [darktable.register_event](darktable.register_event.md).
Events are documented in the [event](../events) section.

* **event_name** - _string_ - The name of the event used to manipulate the event. The combination of event_name and event_type must be unique.
* **event_type** - _string_ - The name of the event to register to.
