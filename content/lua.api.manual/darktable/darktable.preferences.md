---
title: darktable.preferences
id: darktable.preferences
weight: 150
draft: false
author: "people"
---

`table`

Lua allows you to manipulate preferences. Lua has its own namespace for preferences and
you can't access nor write normal darktable preferences.
Preference handling functions take a _script_ parameter. This is a string used to avoid
name collision in preferences \(i.e namespace\). Set it to something unique, usually the
name of the script handling the preference.
Preference handling functions can't guess the type of a parameter. You must pass the type
of the preference you are handling.
Note that the directory, enum, lua and file type preferences are stored internally as string.
The user can only select valid values, but a lua script can set it to any string

# darktable.preferences.register

```
function(
  script : string,
  name : string,
  type : types.lua_pref_type,
  label : string,
  tooltip : string,
  [default : depends on type],
  [min : int or float],
  [max : int or float],
  [step : float],
  [values : string...],
  [widget : types.lua_widget],
  [set_callback : function]
)
```

Creates a new preference entry in the Lua tab of the preference screen. If this function
is not called the preference can't be set by the user \(you can still read and write invisible
preferences\).

* **script** - _string_ - Invisible prefix to guarantee unicity of preferences.
* **name** - _string_ - A unique name used with the script part to identify the preference.
* **type** - _[types.lua_pref_type](../../types/lua_pref_type)_The type of the preference - one of the string values described above.
* **label** - _string_ - The label displayed in the preference screen.
* **tooltip** - _string_ - The tooltip to display in the preference menu.
* **\[default\]** - _Thedepends on type_ - Default value to use when not set explicitly or by the user.
For the enum type of pref, this is mandatory
* **\[mi\]** - _int or float_ - Minimum value \(integer and float preferences only\).
* **\[max\]** - _int or float_ - Maximum value \(integer and float preferences only\).
* **\[step\]** - _float_ - Step of the spinner \(float preferences only\).
* **\[values\]** - _string_ - Other allowed values \(enum preferences only\)
* **\[widget\]** - _[types.lua_widget](../../types/lua_widget)_ - The widget to use in preference \(lua preferences only\)
* **\[set_callback\]** - function_ - A function called when the widget needs to be updated from the preference

\[set_callback\] -

```
function(
  widget : types.lua_widget
)
```

A function called when the widget needs to be updated from the preference

* **widget** - _[types.lua_widget](../../types/lua_widget)_ - The widget to update

# darktable.preferences.read

```
function(
  script : string,
  name : string,
  type : types.lua_pref_type
) : depends on type
```

Reads a value from a Lua preference.

* **script** - _string_ - Invisible prefix to guarantee unicity of preferences.
* **name** - _string_ - The name of the preference displayed in the preference screen.
* **type** - _[types.lua_pref_type](../../types/lua_pref_type)_ - The type of the preference.
* **return** - _depends on type_ - The value of the preference.

# darktable.preferences.write

```
function(
  script : string,
  name : string,
  type : types.lua_pref_type,
  value : depends on type
)
```

Writes a value to a Lua preference.

* **script** - _string_ - Invisible prefix to guarantee unicity of preferences.
* **name** - _string_ - The name of the preference displayed in the preference screen.
* **type** - _[types.lua_pref_type](../../types/lua_pref_type)_ - The type of the preference.
* **value** - _depends on type_ - The value to set the preference to.
