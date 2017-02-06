+++
date = "2016-08-01"
title = "REACH (Data: equipment.lst)"
original_url = "/list/data/equipment.html#reach"
categories = [ "all-tag", "equipment-tag" ]
[menu.main]
    name = "REACH (Data: equipment.lst)"
    parent = "equipment"
+++

## Status

None

## Syntax

`REACH:x`

## Parameters

-   x: Number (Weapon Reach)



<span id="reach"></span> \*\*\* Updated 5.11.6

What it does
------------

The numerical value supplied is used by the
[WEAPONREACH](/list/system/gamemode-miscinfo/weaponreach.html)
miscinfo.lst tag to calculate the reach the wielder gains with the
weapon. In general it adds to the weapon's Reach minus the first 5 feet
of the character's natural reach, so a character with a natural reach of
10 wielding a weapon with a REACH value of 10 will have a reach of 15
with that weapon.

Example
-------

`REACH:10`

Item reaches 10 feet.

