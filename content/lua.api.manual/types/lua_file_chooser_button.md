---
title: lua_file_chooser_button
id: lua_file_chooser_button
weight: 550
draft: false
author: "people"
---

`dt_type`

A button that allows the user to select an existing file

Attributes:

* [has_tostring](../attributes#has_tostring)
* [parent](../attributes#parent) : [types.lua_widget](../types/lua_widget)

# lua_file_chooser_button.\_\_call
see [types.lua_widget.As a function](../types/lua_widget#lua_widgetas-a-function)

# lua_file_chooser_button.extra registration parameters
This widget has no extra registration parameters

# lua_file_chooser_button.title

`string`

The title of the window when choosing a file

Attributes:

* [write](../attributes#write)

# lua_file_chooser_button.value

`string`

The currently selected file

Attributes:

* [write](../attributes#write)

# lua_file_chooser_button.changed_callback
```
function(
 widget : types.lua_widget
)
```

A function to call when the value field changes \(character entered or value selected\)

* **widget** - _[types.lua_widget](../types/lua_widget)_ - The widget that triggered the callback

Attributes:

* [write](../attributes#write)

# lua_file_chooser_button.is_directory

`boolean`

True if the file chooser button only allows directories to be selected

Attributes:

* [write](../attributes#write)
