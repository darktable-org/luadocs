---
title: darktable.gettext
id: darktable.gettext
weight: 80
draft: false
author: "people"
---

`table`

This table contains functions related to translating lua scripts

# darktable.gettext.gettext

```
function(
  msgid : string
) : string
```

Translate a string using the darktable textdomain

* **msgid** - _string_ - The string to translate
* **return** - _string_ - The translated string

# darktable.gettext.dgettext

```
function(
  domainname : string,
  msgid : string
) : string
```

Translate a string using the specified textdomain

* **domainname** - _string_ - The domain to use for that translation
* **msgid** - _string_ - The string to translate
* **return** - _string_ - The translated string

# darktable.gettext.ngettext

```
function(
  msgid : string,
  msgid_plural : string,
  n : int
) : string
```

Translate a string depending on the number of objects using the darktable textdomain

* **msgid** - _string_ - The string to translate
* **msgid_plural** - _string_ - The string to translate in plural form
* **n** - _int_ - The number of objects
* **return** - _string_ - The translated string

# darktable.gettext.dngettext

```
function(
  domainname : string,
  msgid : string,
  msgid_plural : string,
  n : int
) : string
```

Translate a string depending on the number of objects using the specified textdomain 

* **domainname** - _string_ - The domain to use for that translation
* **msgid** - _string_ - The string to translate
* **msgid_plural** - _string_ - The string to translate in plural form
* **n** - _int_ - The number of objects
* **return** - _string_ - The translated string

# darktable.gettext.bindtextdomain

```
function(
  domainname : string,
  dirname : string
)
```

Tell gettext where to find the .mo file translating messages for a particular domain

* **domainname** - _string_ - The domain to use for that translation
* **dirname** - _string_ - The base directory to look for the file. The file should be placed in dirname/locale
name/LC_MESSAGES/domain.mo
