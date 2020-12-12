---
title: escape_xml_characters
id: escape_xml_characters
weight: 20
draft: false
author: "people"
---

## NAME

escape_xml_characters

## SYNOPSIS

escape characters for xml documents

## USAGE
```
local ds = require "lib/dtutils.string"
local result = ds.escape_xml_characters(str)
```
**str** - _string_ - the string that needs escaped

## DESCRIPTION

**escape_xml_characters** provides the escape sequences for
```
"&", '"', "'", "<", and ">" 
```
with the corresponding 
```
"&amp;","&quot;", "&apos;", "&lt;", and "&gt;"
```
.

## RETURN VALUE

**result** - _string_ - the string containing escapes for the xml characters

## REFERENCE

https://stackoverflow.com/questions/1091945/what-characters-do-i-need-to-escape-in-xml-documents
