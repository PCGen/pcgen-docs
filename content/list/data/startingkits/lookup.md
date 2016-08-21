+++
date = "2016-08-01"
title = "LOOKUP (Data: starting_kits.lst)"
original_url = "list/data/startingkits.html#lookup"
categories = [ "all-tag", "startingkits-tag" ]
+++

## Status

None

## Syntax

`LOOKUP:x,y`

## Parameters

-   x: Text (Table name)
-   y: JEP formula or VAR



What it does
------------

Matches the value of the JEP formula or VAR (y variable) with the
associated table's (x variable) `VALUES` tag's upper and lower selection
range and returns the relevant "value".

Example
-------

`LOOKUP:Minor Special Ability (P/S),roll("1d100")`

A random number is generated between 1 and 100 and the item
corresponding to that number will be selected from the "Minor Special
Ability (P/S)" table.

Where it is Used
----------------

GEAR and TABLE lines

