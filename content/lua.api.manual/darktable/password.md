---
title: darktable.password
id: darktable.password
weight: 155
draft: false
author: "people"
---

## Lua API 6.2.0

Store and retrieve credentials using the darktable password storage backend.

# darktable.password.save
```
function(
  application : string,
  username : string,
  password : string
) :boolean
```

Save a username/password pair for use accessing an application.

* **application** - _string_ - Name of application or website.
* **username** - _string_ - The username used to access the application or website.
* **password** - _string_ - The credential used to authenticate the username.
* **return** - _boolean_ - True if the credentials are saved, false if they are not.

# darktable.password.get

```
function(
  application : string,
  username : string
) :string
```

Retrieves the password associated with the username for the application.

* **application** - _string_ - Name of application or website.
* **username** - _string_ - The username used to access the application or website.
* **return** - _string_ - The credentials used to authenticate the user.  Nil is returned if there is an error or the crendentials don't exist.
