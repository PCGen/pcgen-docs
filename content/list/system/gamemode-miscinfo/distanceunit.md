+++
date = "2016-08-01"
title = "DISTANCEUNIT (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#distanceunit"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "DISTANCEUNIT"
    parent = "system_gamemode-miscinfo"
+++

## Status

New 5.9.5

## Syntax

`DISTANCEUNIT:x`

## Parameters

-   x: Text (Distance unit abbreviation).



What it does
------------

Used in UNITSET lines to define the distance unit abbreviation of the
unit set. The string 'unit' is appended to the value and set off from
the value by a space. If you want the unit to follow directly after the
value, prefix the string with '\~'.

Example
-------

`DISTANCEUNIT:ft.`

Defines the distance unit abbreviation as "ft.".

Where it is used
----------------

Used in [UNITSET](/list/system/gamemode-miscinfo/unitset.html) lines.

