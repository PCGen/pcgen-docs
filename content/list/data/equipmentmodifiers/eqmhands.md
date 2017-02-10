+++
date = "2016-08-01"
title = "EQMHANDS (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#eqmhands"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "EQMHANDS"
    parent = "data_equipmentmodifiers"
+++

## Status

None

## Syntax

`BONUS:EQM|HANDS|x|y`

## Parameters

-   x: Number, variable or formula (Number of hands)
-   y: TYPE=Text (Bonus type. Optional.)



What it Does
------------

-   Modifies the number of hands required for the item.
-   See [Global Bonus](/list/global/bonus.html) for more information on
    bonus types.

Examples
--------

`BONUS:EQM|HANDS|1`

Sets the number of hands required by the item to one.

`BONUS:EQM|HANDS|-EQHANDS`

Sets the number of hands required by the item to zero.

