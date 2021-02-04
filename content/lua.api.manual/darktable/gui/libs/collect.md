---
title: darktable.gui.libs.collect
id: collect
weight: 40
draft: false
author: "people"
---

The collection UI element that allows to filter images by collection

Attributes:
* [has_tostring](../../../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../../types/dt_lua_lib_t)

## darktable.gui.libs.collect.filter

```
function(
  [rules : array of types.dt_lib_collect_params_rule_t]
) : array oftypes.dt_lib_collect_params_rule_t
```
Get or change the list of visible images

Attributes:
* [implicit_yield](../../../Attributes#implicit_yield)

* **\[rules\]** - _array of [types.dt_lib_collect_params_rule_t](../../../types/dt_lib_collect_params_rule_t)_ - A table of rules describing the filter. These rules will be applied after this call
* **return** - _array of [types.dt_lib_collect_params_rule_t](../../../types/dt_lib_collect_params_rule_t)_ - The rules that were applied before this call.

## darktable.gui.libs.collect.new_rule

```
function(
) : types.dt_lib_collect_params_rule_t
```

Returns a newly created rule object

* **return** - _[types.dt_lib_collect_params_rule_t](../../../types/dt_lib_collect_params_rule_t)_ - The newly created rule

