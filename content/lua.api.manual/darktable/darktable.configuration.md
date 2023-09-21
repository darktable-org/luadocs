---
title: darktable.configuration
id: darktable.configuration
weight: 30
draft: false
author: "people"
---

`table`

This table includes values that describe details of the configuration of darktable.

# darktable.configuration.version

`string`

The version number of darktable.

# darktable.configuration.has_gui

`boolean`

True if darktable has a GUI \(launched through the main darktable command, not darktable-cli\).

# darktable.configuration.verbose

`boolean`

True if the Lua logdomain is enabled.

# darktable.configuration.tmp_dir

`string`

The name of the directory where darktable will store temporary files.

# darktable.configuration.config_dir

`string`

The name of the directory where darktable will find its global configuration objects \(modules\).

# darktable.configuration.cache_dir

`string`

The name of the directory where darktable stores temporary objects for later reuse.

# darktable.configuration.api_version_major

`number`

The major version number of the lua API.


# darktable.configuration.api_version_minor

`number`

The minor version number of the lua API.

# darktable.configuration.api_version_patch

`number`

The patch version number of the lua API.

# darktable.configuration.api_version_suffix

`string`

The version suffix of the lua API.

# darktable.configuration.api_version_string

`string`

The version description of the lua API. This is a string compatible with the semantic versioning convention

# darktable.configuration.running_os

`string`

The name of the Operating system darktable is currently running on

# darktable.configuration.check_version

```
function(
  module_name : string,
  ... : table...
)
```

Check that a module is compatible with the running version of darktable
Add the following line at the top of your module :
`darktable.configuration.check(...,{M,m,p},{M2,m2,p2})`
To document that your module has been tested with API version M.m.p and M2.m2.p2.
This will raise an error if the user is running a released version of DT and a warning if he
is running a development version
\(the ... here will automatically expand to your module name if used at the top of your script\).

* **module_name** - _string_ - The name of the module to report on error
* **...** - _table_ - Tables of API versions that are known to work with the script
