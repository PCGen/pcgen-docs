+++
date = "2016-08-01"
title = "DAMAGEMULT (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#damagemult"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "DAMAGEMULT"
    parent = "system_gamemode-miscinfo"
+++

## Status

New 5.5.2

## Syntax

`DAMAGEMULT:x=y,x=y`

## Parameters

-   x: Number (number of hands used to wield
    this weapon)
-   y: Number (damage multiplier)



What it does
------------

Used to compute damage multiplier for wielding with two hands vs one
hand, etc.

Example
-------

`DAMAGEMULT:1=1,2=1.5`

The damage multiplier becomes 1.5 if wielded two handed.

Where it is used
----------------

After a WIELDCATEGORY tag.

