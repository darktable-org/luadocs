---
title: gettextExample
id: gettextExample
weight: 30
draft: false
author: "people"
---

## Name

gettextExample.lua - darktable script to show how translations works

## Description

To create the .po file run:
xgettext -l lua gettextExample.lua

xgettext is not a lua tool, it knows (almost) nothing about Lua, and not 
enough to do a proper parsing. It takes a text file (In our case a Lua 
file) and recognises a few (language dependant) keyword in there.
It matches those keywords with internal description on how functions are 
called and creates the .po file accordingly. (For example, it knows that 
the first argument of gettext() is the translated string, but that it's 
the second argument for dgettext)
This is important because it means that if you use some neat Lua tricks
(like renaming functions) xgettext won't recognize those calls and won't 
extract the string to the .po file.
So, this is why we create a local variagle gettext = dt.gettext, so 
xgettext recognises gettext.gettext as a function but not dt.gettext.gettext

To create a .mo file run:
`msgfmt -v gettextExample.po -o gettextExample.mo`

## Usage

* start this script from script manager
* copy the gettextExample.mo to .config/darktable/lua/de_DE/LC_MESSAGES

You need to start darktable with the Lua debug option: darktable -d lua
$LANG must set to: de_DE

The script run on darktable startup and should output this three lines:

```
LUA ERROR Hello World!
LUA ERROR Bild
LUA ERROR Hallo Welt!
```

## Additional Software Required


## Limitations


## Author

Tobias Jakobs

## Change Log
