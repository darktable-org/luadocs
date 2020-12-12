---
title: mkdir
id: mkdir
weight: 150
draft: false
author: "people"
---

## NAME

mkdir

## SYNOPSIS

create the directory(ies) if they do not already exist

## USAGE
```
local df = require "lib/dtutils.file"
df.mkdir(path)
```
**path** - _string_ - a directory path

## DESCRIPTION

**mkdir** creates directories if they do not already exist. It 
creates parent directories if needed.

## RETURN VALUE

_**path** - string_ - a directory path
