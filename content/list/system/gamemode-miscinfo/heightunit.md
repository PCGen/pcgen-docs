+++
date = "2016-08-01"
title = "HEIGHTUNIT (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#heightunit"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "HEIGHTUNIT (Game Mode: miscinfo.lst)"
    parent = "gamemode-miscinfo"
+++

## Status

New 5.9.5

## Syntax

`HEIGHTUNIT:x`

## Parameters

-   x: Text (Height abbreviation).



What it does
------------

Used in UNITSET lines to define the height unit abbreviation of the unit
set. The string 'unit' is appended to the value and set off from the
value by a space. If you want the unit to follow directly after the
value, prefix the string with '\~'. The string 'ftin' is hard-coded to
give results of the format x'y".

Example
-------

`HEIGHTUNIT:cm`

Defines the height unit abbreviation as "cm".

Where it is used
----------------

Used in [UNITSET](/list/system/gamemode-miscinfo/unitset.html) lines.

