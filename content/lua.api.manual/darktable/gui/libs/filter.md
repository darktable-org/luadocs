---
title: darktable.gui.libs.filter
id: filter
weight: 110
draft: false
author: "people"
---

The image-filter menus at the top of the UI

Attributes:
* [has_tostring](../../../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../../types/dt_lua_lib_t)

## darktable.gui.libs.filter.sort

```
function(
  [sort : types.dt_collection_sort_t]
) : types.dt_collection_sort_t
```

Change the collection sort field.

* **\[sort\]** - _[types.dt_collection_sort_t](../../../types/dt_collection_sort_t)_ - The new field to sort by. If empty the current sort field is unchanged
* **return** - _[types.dt_collection_sort_t](../../../types/dt_collection_sort_t)_ = The current sort field.

## darktable.gui.libs.filter.sort_order

```
function(
  [order : types.dt_collection_sort_order_t]
) : types.dt_collection_sort_order_t
```

Change the collection sort order.

* **\[order\]** - _[types.dt_collection_sort_order_t](../../../types/dt_collection_sort_order_t)_ - The order to sort by. If empty the current sort order is unchanged.
* **return** - _[types.dt_collection_sort_order_t](../../../types/dt_collection_sort_order_t)_ - The current sort order.

## darktable.gui.libs.filter.rating

```
function(
  [rating : types.dt_collection_filter_t]
) : types.dt_collection_filter_t
```

Change the collection rating filter.

* **\[rating\]** - _[types.dt_collection_filter_t](../../../types/dt_collection_filter_t)_ - The new rating field to filter by. If empty the current rating field is unchanged.
* **return** - [types.dt_collection_filter_t](../../../types/dt_collection_filter_t) - The current rating field.

## darktable.gui.libs.filter.rating_comparator

```
function(
  [comparator : types.dt_collection_rating_comperator_t]
) : types.dt_collection_rating_comperator_t
```

Change the collection filter comparison field.

* **\[comparator\]** - _[types.dt_collection_rating_comperator_t](../../../types/dt_collection_rating_comperator_t)_ - The new comparison field to filter the rating by. If empty the current rating comparison field is unchanged
* **return** - _[types.dt_collection_rating_comperator_t](../../../types/dt_collection_rating_comperator_t)_ - The current rating comparison field

