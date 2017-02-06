+++
date = "2016-08-01"
title = "EQMARMORACCHECK (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#eqmarmoraccheck"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "EQMARMORACCHECK (Data: equipment_modifiers.lst)"
    parent = "equipmentmodifiers"
+++

## Status

None

## Syntax

`BONUS:EQMARMOR|ACCHECK|x|y`

## Parameters

-   x: Number, variable or formula (Armor
    check penalty)
-   y: TYPE=Text (Bonus type. Optional.)



What it Does
------------

-   Modifies the armor check penalty of the item.
-   See [Global Bonus](/list/global/bonus.html) for more information on
    bonus types.

Example
-------

`BONUS:EQMARMOR|ACCHECK|3`

Decreases the armor check penalty by 3.

`BONUS:EQMARMOR|ACCHECK|2|TYPE=Enhancement`

Decreases the armor check penalty by 2 by enhancement.

