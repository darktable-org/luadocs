---
title: darktable.gui.create_job
id: create_job
weight: 30
draft: false
author: "people"
---

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


