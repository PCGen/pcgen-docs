+++
date = "2016-08-01"
title = "WEIGHTUNIT (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#weightunit"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "WEIGHTUNIT"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_WEIGHTUNIT"
+++

## Status

New 5.9.5

## Syntax

`WEIGHTUNIT:x`

## Parameters

-   x: Text (Weight unit abbreviation).



What it does
------------

Used in UNITSET lines to define the weight unit abbreviation of the unit
set. The string 'unit' is appended to the value and set off from the
value by a space. If you want the unit to follow directly after the
value, prefix the string with '\~'.

Example
-------

`WEIGHTUNIT:lbs.`

Defines the weight unit abbreviation as "lbs.".

Where it is used
----------------

Used in [UNITSET](/list/system/gamemode-miscinfo/unitset.html) lines.

