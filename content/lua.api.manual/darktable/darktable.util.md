---
title: darktable.util
id: darktable.util
weight: 240
draft: false
author: "people"
---

darktable utility functions

# darktable.util.message

```
function(
  sender : string,
  receiver : string,
  message : string
)
```

Sends a message from sender to receiver using the [inter-script-communication](../events/inter-script-communication) event.

* **sender** - _string_ - The module that is sending the message.
* **receiver** - _string_ - The module that the message is intended for or _**broadcast**_ to send to all modules.
* **message** - _string_ - The message for the receiver.

