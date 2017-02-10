+++
date = "2016-08-01"
title = "EQMARMORMAXDEX (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#eqmarmormaxdex"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "EQMARMORMAXDEX"
    parent = "data_equipmentmodifiers"
+++

## Status

None

## Syntax

`BONUS:EQMARMOR|MAXDEX|x|x`

## Parameters

-   x: Number, variable or formula (Max dex modifier)
-   y: TYPE=Text (Bonus type. Optional.)



What it Does
------------

-   Modifies the maximum dexterity applicable to users of the item.
-   See [Global Bonus](/list/global/bonus.html) for more information on
    bonus types.

Example
-------

`BONUS:EQMARMOR|MAXDEX|2`

Increases maximum dexterity bonus of the armor by 2.

`BONUS:EQMARMOR|MAXDEX|2|TYPE=Enhancement`

Increases maximum dexterity bonus of the armor by 2, by enhancement.

