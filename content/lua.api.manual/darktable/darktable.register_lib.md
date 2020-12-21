---
title: darktable.register_lib
id: darktable.register_lib
weight: 60
draft: false
author: "people"
---

```
function(
  plugin_name : string,
  name : string,
  expandable : boolean,
  resettable : boolean,
  containers : table of types.dt_lua_view_t => [ types.dt_ui_container_t, int ],
  widget : types.lua_widget,
  view_enter : function,
  view_leave : function
)
```

Register a new lib object. A lib is a graphical element of darktable's user interface

* **plugin_name** - _string_ - A unique name for your library
* **name** - _string_ - A user-visible name for your library
* **expandable** - _boolean_ - whether this lib should be expandable or not
* **resettable** - _boolean_ - whether this lib has a reset button or not
* **containers** - _table of [types.dt_lua_view_t](../../types/dt_lua_view_t) => \[ [types.dt_ui_container_t](types.dt_ui_container_t), int \]_ - A table associating to each view containing the lib the corresponding container and position.
* **widget** - _[types.lua_widget](../../types/lua_widget_)_ - The widget to display in the lib
* **view_enter** - _[function](#view_enter)_ - A callback called when a view displaying the lib is entered.
* **view_leave** - _[function](#view_leave)_ - A callback called when leaving a view displaying the lib.


# view_enter

```
self:function(
  old_view : types.dt_lua_view_t,
  new_view : types.dt_lua_view_t
)
```

A callback called when a view displaying the lib is entered

* **self** - _[types.dt_lua_lib_t](types.dt_lua_lib_t)_ - The lib on which the callback is called
* **old_view** - _[types.dt_lua_lib_t](types.dt_lua_lib_t)_ - The view that we are leaving
* **new_view** - _[types.dt_lua_lib_t](types.dt_lua_lib_t)_ - The view that we are entering

# view_leave

```
self:function(
  old_view : types.dt_lua_view_t,
  new_view : types.dt_lua_view_t
)
```

A callback called when leaving a view displaying the lib

* **self** - _[types.dt_lua_lib_t](types.dt_lua_lib_t)_ - The lib on which the callback is called
* **old_view** - _[types.dt_lua_lib_t](types.dt_lua_lib_t)_ - The view that we are leaving
* **new_view** - _[types.dt_lua_lib_t](types.dt_lua_lib_t)_ - The view that we are entering
