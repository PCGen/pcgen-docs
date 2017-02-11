+++
date = "2016-08-01"
title = "REACHMULT (Data: equipment.lst)"
original_url = "/list/data/equipment.html#reachmult"
categories = [ "all-tag", "equipment-tag" ]
[menu.main]
    name = "REACHMULT"
    parent = "data_equipment"
    identifier = "data_equipment_REACHMULT"
+++

## Status

None

## Syntax

`REACHMULT:x`

## Parameters

-   x: Number (Weapon Reach Multiplier)



<span id="reachmult"></span> \*\*\* Added 5.11.6

What it does
------------

The numerical value supplied is used by the
[WEAPONREACH](/list/system/gamemode-miscinfo/weaponreach.html)
miscinfo.lst tag to calculate the reach the wielder gains with the
weapon. In general it multiplies the character's natural reach, so a
character with a natural reach of 10 wielding a weapon with a
WEAPONREACH value of 2 will have a reach of 20 with that weapon.

Example
-------

`REACHMULT:2`

Item reaches 2 times the character's normal reach.

