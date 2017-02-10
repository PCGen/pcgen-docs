+++
date = "2016-08-01"
title = "EQMWEAPONCRITRANGEDOUBLE (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#eqmweaponcritrangedouble"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "EQMWEAPONCRITRANGEDOUBLE"
    parent = "data_equipmentmodifiers"
    identifier = "data_equipmentmodifiers_EQMWEAPONCRITRANGEDOUBLE"
+++

## Status

None

## Syntax

`BONUS:EQMWEAPON|CRITRANGEDOUBLE|x|y`

## Parameters

-   x: Number, variable or formula (Critical
    range modifier)
-   y: TYPE=Text (Bonus type. Optional.)



What it Does
------------

-   Modifies the critical range of the item.
-   See [Global Bonus](/list/global/bonus.html) for more information on
    bonus types.

Example
-------

`BONUS:EQMWEAPON|CRITRANGEDOUBLE|1`

Doubles the critical threat range of the weapon.

`BONUS:EQMWEAPON|CRITRANGEDOUBLE|1|TYPE=NonStackingCrit`

Adds one to the non-stacking-critical threat range of the weapon.

