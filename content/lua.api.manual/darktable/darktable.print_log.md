---
title: darktable.print_log
id: darktable.print_log
weight: 180
draft: false
author: "people"
---

```
function(
  message : string
)
```

This function will print its parameter if the Lua logdomain is activated. Start darktable
with the `"-d lua"` command line option to enable the Lua logdomain.

* **message** - _string_ - The string to display.

