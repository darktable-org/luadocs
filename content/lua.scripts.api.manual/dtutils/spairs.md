---
title: spairs
id: spairs
weight: 60
draft: false
author: "people"
---
## NAME

spairs

## SYNOPSIS

an iterator that provides sorted pairs from a table

## USAGE
```
local du = require "lib/dtutils"
for key, value in du.spairs(t, order) do
  -- do something
end
```
**t** - _table_ - table of key, value pairs
**order** - _function_ - an optional function to sort the pairs, if none is supplied, table.sort() is used

## DESCRIPTION

**spairs** is an iterator that returns key, value pairs from a table in sorted
order.  The sorting order is the result of **table.sort()** if no function is 
supplied, otherwise sorting is done as specified in the function.

## EXAMPLE
```
HighScore = { Robin = 8, Jon = 10, Max = 11 }
-- basic usage, just sort by the keys
for k,v in spairs(HighScore) do
  print(k,v)
end
--> Jon     10  
--> Max     11  
--> Robin   8  
-- this uses an custom sorting function ordering by score descending
for k,v in spairs(HighScore, function(t,a,b) return t[b] < t[a] end) do
  print(k,v)
end
--> Max     11
--> Jon     10
--> Robin   8
```
## REFERENCE

Code copied from http://stackoverflow.com/questions/15706270/sort-a-table-in-lua