+++
date = "2016-08-01"
title = "EQMWEIGHTDIV (Data: equipment_modifiers.lst)"
original_url = "list/data/equipmentmodifiers.html#eqmweightdiv"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
+++

## Status

None

## Syntax

`BONUS:EQM|WEIGHTDIV|x|y`

## Parameters

-   x: Number, variable or formula (Weight divisor)
-   y: TYPE=Text (Bonus type. Optional.)



What it Does
------------

-   Modifies the weight of the item.
-   See [Global Bonus](/list/global/bonus.html) for more information on
    bonus types.

Example
-------

`BONUS:EQM|WEIGHTDIV|2`

Divides the weight of the item in half.

`BONUS:EQM|WEIGHTDIV|2|TYPE=Enhancement.REPLACE`

Divides the weight of the item in half, replaces the original amount by
enhancement.

