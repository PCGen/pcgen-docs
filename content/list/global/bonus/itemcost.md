+++
date = "2016-08-01"
title = "ITEMCOST (Global: BONUS)"
original_url = "/list/global/bonus.html#itemcost"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "ITEMCOST"
    parent = "global_bonus"
    identifier = "global_bonus_ITEMCOST"
+++

## Status

None

## Syntax

`BONUS:ITEMCOST|TYPE.x.x|y`

## Parameters

-   x: Text (Item Type)
-   y: Number, variable or formula (Cost formula)



What it Does
------------

Used in Equipment and Equipment Modifiers, applies the cost formula to
the equipment if it has all the listed types. Any formula that is valid
in an [EQMOD COST](/list/data/equipmentmodifiers/cost.html) tag can be
used.

Example
-------

`BONUS:ITEMCOST|TYPE.Weapon|200`

Adds 200 to the cost if the item has the Weapon type.

`BONUS:ITEMCOST|TYPE.Armor.Light|BASECOST*2`

Doubles the cost if the item has the Armor and Light types.

