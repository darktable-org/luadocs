---
title: inter-script-communication
id: inter-script-communication
weight: 45
draft: false
author: "people"
---

`event`

This event is called to send messages back and forth between scripts.

# inter-script-communication.callback

```
function(
  event : string,
  sender : string,
  receiver : string,
  message : string
)
```

* **event** - _string_ - The name of the event that triggered the callback.
* **sender** - _string_ - The name of the module sending the event.
* **receiver** - _string_ - The name of the module that the event is being sent to or _**broadcast**_ for all modules.
* **message** - _string_ - The message intended for the receiving module

# inter-script-communication.extra registration parameters

This event has no extra registration parameters.

