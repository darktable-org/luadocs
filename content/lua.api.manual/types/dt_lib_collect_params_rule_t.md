---
title: dt_lib_collect_params_rule_t
id: dt_lib_collect_params_rule_t
weight: 400
draft: false
author: "people"
---

`dt_type`

A single rule for filtering a collection

# dt_lib_collect_params_rule_t.mode

[types.dt_lib_collect_mode_t](../types/dt_lib_collect_mode_t)

How this rule is applied after the previous one. Unused for the first rule

Attributes:

* [write](../attributes#write)

# dt_lib_collect_params_rule_t.data

`string`

The text segment of the rule. Exact content depends on the type of rule

Attributes:

* [write](../attributes#write)

# dt_lib_collect_params_rule_t.item

[types.dt_collection_properties_t](../types/dt_collection_properties_t)

The item on which this rule filter. i.e the type of the rule

Attributes:

* [write](../attributes#write)

