+++
date = "2016-08-01"
title = "CONTAINS (Game Mode: equipmentslots.lst)"
original_url = "/list/system/gamemode-equipmentslots.html#contains"
categories = [ "all-tag", "gamemode-equipmentslots-tag" ]
[menu.main]
    name = "CONTAINS (Game Mode: equipmentslots.lst)"
    parent = "gamemode-equipmentslots"
+++

## Status

None

## Syntax

`CONTAINS:x,x=y`

## Parameters

-   x: Text (Equipment type)
-   y: Number (Number of such types the slot can hold)



What it does
------------

-   This tag follows the `EQSLOT` tag and sets what equipment type, and
    how many, the slot holds.
-   Multiple equipment types may be included in a comma-delimited (,)
    list.

Example
-------

`CONTAINS:Eyegear=1`

This slot can hold 1 item of type Eyegear.

`CONTAINS:Armor,Robe=1`

This slot can hold 1 item of type Armor or Robe.

