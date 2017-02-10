+++
date = "2016-08-01"
title = "EQMWEIGHTADD (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#eqmweightadd"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "EQMWEIGHTADD"
    parent = "data_equipmentmodifiers"
    identifier = "data_equipmentmodifiers_EQMWEIGHTADD"
+++

## Status

None

## Syntax

`BONUS:EQM|WEIGHTADD|x|y`

## Parameters

-   x: Number, variable or formula (Weight added)
-   y: TYPE=Text (Bonus type. Optional.)



What it Does
------------

-   Modifies the weight of the item.
-   See [Global Bonus](/list/global/bonus.html) for more information on
    bonus types.

Example
-------

`BONUS:EQM|WEIGHTADD|0.5`

Adds half a weight unit to the item's weight.

`BONUS:EQM|WEIGHTADD|-10|TYPE=Enhancement`

Subtracts 10 from the item's weight due to enhancement.

