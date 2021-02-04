---
title: darktable.control
id: darktable.control
weight: 40
draft: false
author: "people"
---

This table contain function to manipulate the control flow of lua programs. It provides
ways to do background jobs and other related functions

# darktable.control.ending

`boolean`

TRUE when darktable is terminating
Use this variable to detect when you should finish long running jobs

# darktable.control.dispatch

```
function(
  function : function,
  ... : anything
)
```

Runs a function in the background. This function will be run at a later point, after luarc has
finished running. If you do a loop in such a function, please check darktable.control.ending
in your loop to finish the function when darktable exits

* **function** - _function_ - The call to dispatch
* **...** - _anything_ - extra parameters to pass to the function

# darktable.control.sleep

```
function(
  delay : int
)
```

Suspends execution while not blocking darktable

* **delay** - _int_ - The delay in millisecond to sleep

# darktable.control.execute

```
function(
  command : string
) : int
```

Run a command in a shell while not blocking darktable

* **command** - _string_ - The command to run, as in 'sh -c'
* **return** - _int_ - The result of the system call

# darktable.control.read

```
function(
  file : file
)
```

Block until a file is readable while not blocking darktable
This function is not available on Windows builds

* **file** - _file_ - The file object to wait for
