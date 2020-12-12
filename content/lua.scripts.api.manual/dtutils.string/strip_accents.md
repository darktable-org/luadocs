---
title: strip_accents
id: strip_accents
weight: 60
draft: false
author: "people"
---

## NAME

strip_accents

## SYNOPSIS

strip accents from characters

## USAGE
```
local ds = require "lib/dtutils.string"
local result = ds.strip_accents(str)
```
**str** - _string_ - the string with characters that need accents removed

## DESCRIPTION

**strip_accents** removes accents from accented characters returning the 
unaccented character.

## RETURN VALUE

**result** - _string_ - the string containing unaccented characters

## REFERENCE

Copied from https://forums.coronalabs.com/topic/43048-remove-special-characters-from-string/
