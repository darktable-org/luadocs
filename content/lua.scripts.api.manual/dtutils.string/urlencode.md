---
title: urlencode
id: urlencode
weight: 70
draft: false
author: "people"
---

## NAME

urlencode

## SYNOPSIS

encode a string in a websage manner

## USAGE
```
local ds = require "lib/dtutils.string"
local result = ds.urlencode(str)
```
**str** - _string_ - the string that needs to be made websafe

## DESCRIPTION

**urlencode** converts a string into a websafe version suitable for
use in a web browser.

## RETURN VALUE

**result** - _string_ - a websafe string

## REFERENCE

https://forums.coronalabs.com/topic/43048-remove-special-characters-from-string