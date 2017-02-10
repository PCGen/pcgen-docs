+++
date = "2016-08-01"
title = "EQMWEIGHTMULT (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#eqmweightmult"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "EQMWEIGHTMULT"
    parent = "data_equipmentmodifiers"
    identifier = "data_equipmentmodifiers_EQMWEIGHTMULT"
+++

## Status

None

## Syntax

`BONUS:EQM|WEIGHTMULT|x|y`

## Parameters

-   x: Number, variable or formula (Weight multiplier)
-   y: TYPE=Text (Bonus type. Optional.)



What it Does
------------

-   Modifies the weight of the item.
-   See [Global Bonus](/list/global/bonus.html) for more information on
    bonus types.

Example
-------

`BONUS:EQM|WEIGHTMULT|2`

Doubles the weight of the item.

`BONUS:EQM|WEIGHTMULT|1.2|TYPE=Enhancement`

Multiples the weight of the item by 1.2 by enhancement.

