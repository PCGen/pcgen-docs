+++
date = "2016-08-01"
title = "EQMWEAPONRANGEADD (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#eqmweaponrangeadd"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "EQMWEAPONRANGEADD"
    parent = "data_equipmentmodifiers"
+++

## Status

None

## Syntax

`BONUS:EQMWEAPON|RANGEADD|x|y`

## Parameters

-   x: Number, variable or formula (Range modifier)
-   y: TYPE=Text (Bonus type. Optional.)



What it Does
------------

-   Modifies the range of the item.
-   See [Global Bonus](/list/global/bonus.html) for more information on
    bonus types.

Example
-------

`BONUS:EQMWEAPON|RANGEADD|10`

Adds 10 distance units to the weapon's range.

`BONUS:EQMWEAPON|RANGEADD|5|TYPE=CONVERSION`

Adds 5 distance units to the weapon's range by conversion.

