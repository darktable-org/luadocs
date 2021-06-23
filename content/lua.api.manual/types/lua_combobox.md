---
title: lua_combobox
id: lua_combobox
weight: 520
draft: false
author: "people"
---

`dt_type`

A widget with multiple text entries in a menu.
This widget can be set as editable at construction time.
If it is editable the user can type a value and is not constrained by the values in the menu.

Attributes:

* [has_tostring](../attributes#has_tostring)
* [parent](../attributes#parent) : [types.lua_widget](../types/lua_widget)

# lua_combobox.\_\_call
see [types.lua_widget.As a function](../types/lua_widget#lua_widgetas-a-function)

# lua_combobox.extra registration parameters
This widget has no extra registration parameters

# lua_combobox.value

`string`

The text content of the selected entry, can be nil.
You can set it to a number to select the corresponding entry from the menu.
If the combobox is editable, you can set it to any string.
You can set it to nil to deselect all entries.

Attributes:

* [write](../attributes#write)

# lua_combobox.selected

`integer`

The index of the selected entry, or 0 if nothing is selected.
You can set it to a number to select the corresponding entry from the menu, or to 0 to
select nothing.
You can set it to nil to deselect all entries.

Attributes:

* [write](../attributes#write)

# lua_combobox.#

`string`

The various menu entries.
You can add new entries by writing to the first element beyond the end.
You can removes entries by setting them to nil.

Attributes:

* [write](../attributes#write)

# lua_combobox.changed_callback
```
function(
  widget : types.lua_widget
)
```
A function to call when the value field changes \(character entered or value selected\)

* **widget** - _[types.lua_widget](../types/lua_widget)_ - The widget that triggered the callback

Attributes:

* [write](../attributes#write)

# lua_combobox.editable

`boolean`

True is the user is allowed to type a string in the combobox

Attributes:

* [write](../attributes#write)

# lua_combobox.label

`string`

The label displayed on the combobox

Attributes:

* [write](../attributes#write)

