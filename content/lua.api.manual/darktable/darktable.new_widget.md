---
title: darktable.new_widget
id: darktable.new_widget
weight: 100
draft: false
author: "people"
---

```
function(
  type : string,
  ... : variable
) : types.lua_widget
```

Creates a new widget object to display in the UI.

* **type** - _string_ - The type of storage object to create, one of:
  * box
  * button
  * check_button
  * combobox
  * container
  * entry
  * file_chooser_button
  * label
  * section_label
  * separator
  * slider
  * stack
  * text_view

* **...** - _variable_ - Extra parameters, exact value are documented with each type
* **return** - _[types.lua_widget](../../types/lua_widget)_ - The newly created object. Exact type depends on the type passed

