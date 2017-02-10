+++
date = "2016-08-01"
title = "BONUSITEMCOST (System: sizeAdjustment.lst)"
original_url = "/list/system/sizeadjustment.html#bonusitemcost"
categories = [ "all-tag", "sizeadjustment-tag" ]
[menu.main]
    name = "BONUSITEMCOST"
    parent = "system_sizeadjustment"
    identifier = "system_sizeadjustment_BONUSITEMCOST"
+++

## Status

None

## Syntax

`None`

## Parameters




<span id="bonusitemcost"></span>

### BONUS:ITEMCOST

Modifies the cost of items based on the item's size category, i.e. the
size of the creature the item was made for.

For example, in 3.5e, a large-sized weapon [costs twice as
much](http://www.d20srd.org/srd/equipment/weapons.htm#cost) as a
medium-sized weapon, and large-sized armour [costs twice as
much](http://www.d20srd.org/srd/equipment/armor.htm#armorForUnusualCreatures)
as medium-sized armour.

Only works in `sizeAdjustment.lst`.

#### Status {#status-4}

New in 5.10.1

#### Syntax {#syntax-6}

`BONUS:ITEMCOST|TYPE=item_type_1,TYPE=item_type_2,...|cost_multiplier`

-   `item_type` is a type of equipment from the data set's equipment
    files, i.e. the `35e` files `rsrd_equip_arms_and_armor.lst` ,
    `rsrd_equip_general.lst` , and `rsrd_equip_magic_items.lst` . Such
    types might include:
    -   `Armor`
    -   `Weapon`
    -   `Potion`
    -   Very specific types such as `Quarterstaff` .
-   `cost_multiplier` is a number.

#### Examples {#examples-2}

-   `BONUS:ITEMCOST|TYPE=Weapon|0.5`

Halves the cost of weapons.

-   `BONUS:ITEMCOST|TYPE=Weapon,TYPE=Armor|2`

Doubles the cost of weapons and armour.

-   `BONUS:ITEMCOST|TYPE=Scrolls,TYPE=Potions|1`

Leaves the cost of scrolls and potions un-modified.

-   `BONUS:ITEMCOST|TYPE=Alchemical,TYPE=Liquid,TYPE=Clothing,TYPE=Food|2`

Doubles the costs of all items of type Alchemical, Liquid, Clothing, or
Food.

