+++
date = "2016-08-01"
title = "EQMARMORSPELLFAILURE (Data: equipment_modifiers.lst)"
original_url = "list/data/equipmentmodifiers.html#eqmarmorspellfailure"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
+++

## Status

None

## Syntax

`BONUS:EQMARMOR|SPELLFAILURE|x|y`

## Parameters

-   x: Number, variable or formula (Spell
    failure modifier)
-   y: TYPE=Text (Bonus type. Optional.)



What it Does
------------

-   Modifies the spell failure percentage applicable to users of
    the item.
-   See [Global Bonus](/list/global/bonus.html) for more information on
    bonus types.

Example
-------

`BONUS:EQMARMOR|SPELLFAILURE|-10`

Decreases the spell failure chance of the armor by 10%.

`BONUS:EQMARMOR|SPELLFAILURE|-10|TYPE=Enhancement`

Decreases the spell failure chance of the armor by 10% by enhancement.

