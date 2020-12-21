---
title: darktable.gui
id: darktable.gui
weight: 110
draft: false
author: "people"
---

This subtable contains function and data to manipulate the darktable user interface with
Lua.
Most of these function won't do anything if the GUI is not enabled (i.e you are using the
command line version darktable-cli instead of darktable).

# darktable.gui.action_images

`table`

A table of [types.dt_lua_image_t](../../types/dt_lua_image_t) on which the user expects UI actions to happen.
It is based on both the hovered image and the selection and is consistent with the way
darktable works.
It is recommended to use this table to implement Lua actions rather than [darktable.gui.hovered](#darktable.gui.hovered) or [darktable.gui.selection](#darktable.gui.selection) to be consistent with darktable's GUI.

# darktable.gui.hovered

`types.dt_lua_image_t`

The image under the cursor or nil if no image is hovered.

# darktable.gui.selection

```
function(
  [selection : table of types.dt_lua_image_t]
) : table of types.dt_lua_image_t
```

Get or change the set of selected images.

Attributes: [implicit_yield](../Attributes#implicit_yield)

* **\[selection\]** - _table of [types.dt_lua_image_t](../../types/dt_lua_image_t)_ - A table of images which will define the selected images. If this parameter is not given
the selection will be untouched. If an empty table is given the selection will be emptied.
* **return** - _table of [types.dt_lua_image_t](../../types/dt_lua_image_t)_ - A table containing the selection as it was before the function was called.

# darktable.gui.current_view

```
function(
  [view : types.dt_lua_view_t]
) : types.dt_lua_view_t
```

Get or change the current view.

* **\[view\]** - [_types.dt_lua_view_t](../../types/dt_lua_view_t)_ - The view to switch to. If empty the current view is unchanged
* **return** - [_types.dt_lua_view_t](../../types/dt_lua_view_t)_ - the current view

# darktable.gui.panel_visible

```
function(
  panel : types.dt_ui_panel_t
) : boolean
```

Determines if the specified panel is visible.

* **panel** - _[types.dt_ui_panel_t](../../types/dt_ui_panel_t)_ - The panel to check.
* **return** - _boolean_ - true if the panel is visible, false if not

# darktable.gui.panel_hide

```
function(
panel : types.dt_ui_panel_t
)
```

Hides the specified panel.

* **panel** - _[types.dt_ui_panel_t](../../types/dt_ui_panel_t)_ - The panel to hide.

# darktable.gui.panel_show

```
function(
panel : types.dt_ui_panel_t
)
```

Shows the specified panel.

* **panel** - _[types.dt_ui_panel_t](../../types/dt_ui_panel_t)_ - The panel to show.

# darktable.gui.panel_hide_all

```
function(
)
```

Hide all panels.

# darktable.gui.panel_show_all

```
function(
)
```
Show all panels.

# darktable.gui.panel_get_size

```
function(
  panel : types.dt_ui_panel_t
):int
```

Gets the size in pixels of the specified panel. This only works for the left, right, and bottom
panels.

* **panel** - _[types.dt_ui_panel_t](../../types/dt_ui_panel_t)_ - The panel to get the size of.

# darktable.gui.panel_set_size

```
function(
  panel : types.dt_ui_panel_t
  size : int
)
```

Sets the size in pixels of the specified panel. This only works for the left, right, and bottom
panels.

* **panel** - _[types.dt_ui_panel_t](../../types/dt_ui_panel_t)_ - The panel to set the size of.
* **size** - _int_ - The size to set the panel to.

# darktable.gui.create_job

```
function(
  text : string,
  [percentage : boolean],
  [cancel_callback : function]
) : types.dt_lua_backgroundjob_t
```

Create a new progress_bar displayed in [darktable.gui.libs.backgroundjobs](#darktable.gui.libs.backgroundjobs)

* **text** - _string_ - The text to display in the job entry
* **\[percentage\]** - _boolean_ - Should a progress bar be displayed
* **\[cancel_callback\]** - _[function](#cancel_callback)_ - A function called when the cancel button for that job is pressed.  Note: the job won't be destroyed automatically. You need to set [types.dt_lua_backgroundjob_t.valid](../../types/dt_lua_backgroundjob_t#valid) to false for that.

* **return** - _[types.dt_lua_backgroundjob_t](../../types/dt_lua_backgroundjob_t)_ - The newly created job object

## cancel_callback
```
function(
  job : types.dt_lua_backgroundjob_t
)
```

* **job** - _[types.dt_lua_backgroundjob_t](../../types/dt_lua_backgroundjob_t)_ - The job who is being cancelled


# darktable.gui.views

The different views in darktable

## darktable.gui.views.map

The map view

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#paren) : [types.dt_lua_view_t](../../types/dt_lua_view_t)

### darktable.gui.views.map.latitude

* number - The latitude of the center of the map

Attributes:
* [write](../Attributes#write)

### darktable.gui.views.map.longitude

* number - The longitude of the center of the map

Attributes:
* [write](../Attributes#write)

### darktable.gui.views.map.zoom

* number - The current zoom level of the map

Attributes:
* [write](../Attributes#write)

## darktable.gui.views.darkroom

The darkroom view

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_view_t](../../types/dt_lua_view_t)

### darktable.gui.views.darkroom.display_image

```
function(
  [image : types.dt_lua_image_t]
) : types.dt_lua_image_t
```

Display an image in darkroom view.
* **\[image\] - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The image to be displayed. If the image is not given, nothing will be changed.
* **return** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The image currently displayed.

## darktable.gui.views.lighttable

The lighttable view

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_view_t](../../types/dt_lua_view_t)

### darktable.gui.views.lighttable.is_image_visible

```
function(
  image : types.dt_lua_image_t
) : types.dt_lua_image_t
```

Check if the image is visible in lighttable view. The lighttable must be in file manager or
zoomable mode.

* **image** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The image to be checked.
* **return** - _boolean_ - True if the image is displayed. False if the image is partially displayed or not displayed.

### darktable.gui.views.lighttable.set_image_visible

```
function(
  image : types.dt_lua_image_t
) : types.dt_lua_image_t
```

Set the image visible in lighttable view. The lighttable must be in file manager or zoomable
mode.

* **image** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The image to set visible.
* **return** - _int_ - An error is returned if no image is specified.

## darktable.gui.views.tethering

The tethering view

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_view_t](../../types/dt_lua_view_t)

## darktable.gui.views.slideshow

The slideshow view

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_view_t](../../types/dt_lua_view_t)

## darktable.gui.views.print

The print view

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_view_t](../../types/dt_lua_view_t)

# darktable.gui.libs

This table allows referencing all lib objects.
lib objects are the graphical blocks within each view.
To quickly figure out which lib is which, you can use the following code, which will make a
given lib blink.

```
local dt = require "darktable"
local tested_module="global_toolbox"
dt.gui.libs[tested_module].visible=false
dt.control.sleep(2000)
while true do
  dt.gui.libs[tested_module].visible = not dt.gui.libs[tested_module].visible
  dt.control.sleep(2000)
end
```

### darktable.gui.libs.snapshots

The UI element that manipulates snapshots in darkroom

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

### darktable.gui.libs.snapshots.ratio

number - The place in the screen where the line separating the snapshot is. Between 0 and 1

Attributes:
* [write](../Attributes#write)

darktable.gui.libs.snapshots.direction

[types.snapshot_direction_t](../../types/snapshot_direction_t) - The direction of the snapshot overlay

Attributes:
* [write](../Attributes#write)

### darktable.gui.libs.snapshots.#

[types.snapshot_direction_t](../../types/snapshot_direction_t) - The different snapshots for the image

### darktable.gui.libs.snapshots.selected

[types.snapshot_direction_t](../../types/snapshot_direction_t) - The currently selected snapshot

### darktable.gui.libs.snapshots.take_snapshot

```
function(
)
```

Take a snapshot of the current image and add it to the UI
The snapshot file will be generated at the next redraw of the main window

### darktable.gui.libs.snapshots.max_snapshot

number - The maximum number of snapshots

## darktable.gui.libs.collect

The collection UI element that allows to filter images by collection

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

### darktable.gui.libs.collect.filter

```
function(
  [rules : array of types.dt_lib_collect_params_rule_t]
) : array oftypes.dt_lib_collect_params_rule_t
```
Get or change the list of visible images

Attributes:
* [implicit_yield](../Attributes#implicit_yield)

* **\[rules\]** - _array of [types.dt_lib_collect_params_rule_t](../../types/dt_lib_collect_params_rule_t)_ - A table of rules describing the filter. These rules will be applied after this call
* **return** - _array of [types.dt_lib_collect_params_rule_t](../../types/dt_lib_collect_params_rule_t)_ - The rules that were applied before this call.

### darktable.gui.libs.collect.new_rule

```
function(
) : types.dt_lib_collect_params_rule_t
```

Returns a newly created rule object

* **return** - _[types.dt_lib_collect_params_rule_t](../../types/dt_lib_collect_params_rule_t)_ - The newly created rule

## darktable.gui.libs.import

The buttons to start importing images

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

### darktable.gui.libs.import.register_widget

```
function(
  widget : types.lua_widget
)
```

Add a widget in the option expander of the import dialog

* **widget** - _[types.lua_widget](../../types/lua_widget)_ - The widget to add to the dialog. The reset callback of the widget will be called whenever the dialog is opened.

## darktable.gui.libs.styles

The style selection menu

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.metadata_view

The widget displaying metadata about the current image

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

### darktable.gui.libs.metadata_view.register_info

```
function(
  name : string,
  callback : function
)
```

Register a function providing extra info to display in the widget

* **name** - _string_ - The name displayed for the new information
* **callback** - _function_ - The function providing the info

callback -

```
function(
  image : types.dt_lua_image_t
) : string
```

* **image** - _[types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The image to analyze
* **return** - _string_ - The extra information to display

## darktable.gui.libs.metadata

The widget allowing modification of metadata fields on the current image

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.hinter

The small line of text at the top of the UI showing the number of selected images

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.filmstrip

The filmstrip at the bottom of some views

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.viewswitcher

The labels allowing to switch view

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.darktable_label

The darktable logo in the upper left corner

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.tagging

The tag manipulation UI

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.geotagging

The geotagging time synchronisation UI

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.recentcollect

The recent collection UI element

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.global_toolbox

The common tools to all view \(settings, grouping...\)

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

### darktable.gui.libs.global_toolbox.grouping

boolean- The current status of the image grouping option

Attributes:
* [write](../Attributes#write)

### darktable.gui.libs.global_toolbox.show_overlays

boolean - the current status of the image overlays option

Attributes:
* [write](../Attributes#write)

## darktable.gui.libs.filter

The image-filter menus at the top of the UI

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

### darktable.gui.libs.filter.sort

```
function(
  [sort : types.dt_collection_sort_t]
) : types.dt_collection_sort_t
```

Change the collection sort field.

* **\[sort\]** - _[types.dt_collection_sort_t](../../types/dt_collection_sort_t)_ - The new field to sort by. If empty the current sort field is unchanged
* **return** - _[types.dt_collection_sort_t](../../types/dt_collection_sort_t)_ = The current sort field.

### darktable.gui.libs.filter.sort_order

```
function(
  [order : types.dt_collection_sort_order_t]
) : types.dt_collection_sort_order_t
```

Change the collection sort order.

* **\[order\]** - _[types.dt_collection_sort_order_t](../../types/dt_collection_sort_order_t)_ - The order to sort by. If empty the current sort order is unchanged.
* **return** - _[types.dt_collection_sort_order_t](../../types/dt_collection_sort_order_t)_ - The current sort order.

### darktable.gui.libs.filter.rating

```
function(
  [rating : types.dt_collection_filter_t]
) : types.dt_collection_filter_t
```

Change the collection rating filter.

* **\[rating\]** - _[types.dt_collection_filter_t](../../types/dt_collection_filter_t)_ - The new rating field to filter by. If empty the current rating field is unchanged.
* **return** - [types.dt_collection_filter_t](../../types/dt_collection_filter_t) - The current rating field.

### darktable.gui.libs.filter.rating_comparator

```
function(
  [comparator : types.dt_collection_rating_comperator_t]
) : types.dt_collection_rating_comperator_t
```

Change the collection filter comparison field.

* **\[comparator\]** - _[types.dt_collection_rating_comperator_t](../../types/dt_collection_rating_comperator_t)_ - The new comparison field to filter the rating by. If empty the current rating comparison field is unchanged
* **return** - _[types.dt_collection_rating_comperator_t](../../types/dt_collection_rating_comperator_t)_ - The current rating comparison field

## darktable.gui.libs.ratings

The stars to set the rating of an image

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.select

The buttons that allow to quickly change the selection

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

### darktable.gui.libs.select.register_selection

```
function(
  label : string,
  callback : function,
  [tooltip : string]
)
```

Add a new button and call a callback when it is clicked

* **label** - _string_ - The label to display on the button
* **callback** - _function_ - The function to call when the button is pressed
* **\[tooltip\]** - _string_ - The tooltip to use on the new button

callback -

```
function(
  event : string,
  images : table oftypes.dt_lua_image_t
) : table oftypes.dt_lua_image_t
```

The function to call when the button is pressed

* **event** - _string_ - The name of the button that was pressed
* **images** - _table of [types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The images in the current collection. This is the same content asdarktable.collection
* **return** - _table of [types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The images to set the selection to

## darktable.gui.libs.colorlabels

The color buttons that allow to set labels on an image

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.lighttable_mode

The navigation and zoom level UI in lighttable

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

### darktable.gui.libs.lighttable_mode.layout

```
function(
  [layout : types.dt_lighttable_layout_t]
) : types.dt_lighttable_layout_t
```

Change the lighttable layout.

* **\[layout\]** - _[types.dt_lighttable_layout_t](../../types/dt_lighttable_layout_t)_ - The layout to switch to. If empty the current layout is unchanged
* **return** - _[types.dt_lighttable_layout_t](../../types/dt_lighttable_layout_t)_ - the current layout

### darktable.gui.libs.lighttable_mode.zoom_level

```
function(
  [level : int]
) : int
```

Change the lighttable zoom level.

* **\[level\]** - _int_ - The zoom level to switch to. If empty the current zoom level is unchanged
* **return** - _int_ - the current zoom level

## darktable.gui.libs.copy_history

The UI element that manipulates history

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.image

The UI element that manipulates the current images

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

### darktable.gui.libs.image.register_action

```
function(
  label : string,
  callback : function,
  [tooltip : string]
)
```

Add a new button and call a callback when it is clicked

* **label** - _string_ - The label to display on the button
* **callback** - _function_ - The function to call when the button is pressed
* **\[tooltip\]** - _string_ - The tooltip to use on the new button

callback -

```
function(
  event : string,
  images : table oftypes.dt_lua_image_t
)
```

The function to call when the button is pressed

* **event** - _string_ - The name of the button that was pressed
* **images** - _table of [types.dt_lua_image_t](../../types/dt_lua_image_t)_ - The images to act on when the button was clicked

## darktable.gui.libs.modulegroups

The icons describing the different iop groups

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.module_toolbox

The tools on the bottom line of the UI (overexposure)

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.session

The session UI when tethering

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)


## darktable.gui.libs.histogram

The histogram widget

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.export

The export menu

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.history

The history manipulation menu

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.colorpicker

The colorpicker menu

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.navigation

The full image preview to allow navigation

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.masks

The masks window

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.view_toolbox

The view_toolbox window

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.live_view

The liveview window

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.map_settings

The map setting window

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.camera

The camera selection UI

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.location

The location ui

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.backgroundjobs

The window displaying the currently running jobs

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)

## darktable.gui.libs.print_settings

The settings window in the print view

Attributes:
* [has_tostring](../Attributes#has_tostring)
* [parent](../Attributes#parent) : [types.dt_lua_lib_t](../../types/dt_lua_lib_t)
