---
title: darktable.debug
id: darktable.debug
weight: 210
draft: false
author: "people"
---

`table`

This section must be activated separately by calling require `darktable.debug`

# darktable.debug.dump

```
function(
  object : anything,
  [name : string],
  [known : table]
) : string
```

This will return a string describing everything Lua knows about an object, used to know
what an object is. This function is recursion-safe and can be used to dump \_G if needed.

* **object** - _anything_ - The object to dump.
* **\[name\]** - _string_ - A name to use for the object.
* **\[known\]** - _table_ - A table of object,string pairs. Any object in that table will not be dumped, the string
will be printed instead.
defaults to darktable.debug.known if not set
* **return** - _string_ - A string containing a text description of the object - can be very long.

# darktable.debug.debug

`boolean`

Initialized to false; set it to true to also dump information about metatables.

# darktable.debug.max_depth

`number`

Initialized to 10; The maximum depth to recursively dump content.

# darktable.debug.known

`table`

A table containing the default value of darktable.debug.dump.known

# darktable.debug.type

```
function(
  object : anything
) : string
```

Similar to the system function type\(\) but it will return the real type instead of _userdata_
for darktable specific objects.

* **object** - _anything_ - The object whose type must be reported.
* **return** - _string_ - A string describing the type of the object.
