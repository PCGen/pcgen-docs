+++
date = "2016-08-01"
title = "BONUSITEMWEIGHT (System: sizeAdjustment.lst)"
original_url = "list/system/sizeadjustment.html#bonusitemweight"
categories = [ "all-tag", "sizeadjustment-tag" ]
+++

## Status

None

## Syntax

`None`

## Parameters




<span id="bonusitemweight"></span>

### BONUS:ITEMWEIGHT

Modifies the weight of of items based on the item's size category, i.e.
the size of the creature the item was made for.

For example, in 3.5e, armour for small-size creatures [weighs half as
much](http://www.d20srd.org/srd/equipment/armor.htm#armorForUnusualCreatures)
as armour for medium-sized creatures.

Only works in `sizeAdjustment.lst`.

#### Status {#status-5}

New in 5.10.1.

#### Syntax {#syntax-7}

`BONUS:ITEMWEIGHT|TYPE=item_type_1,TYPE=item_type_2,...|weight_multiplier`

-   `item_type` is a type of equipment from the data set's equipment
    files, as per `BONUS:ITEMCOST` above.
-   `weight_multiplier` is a number.

#### Example {#example-3}

-   `ITEMWEIGHT|TYPE=Armor|2`

Doubles the weight of armour made for a creature of this size.

-   `ITEMWEIGHT|TYPE=Resizable|0.25`

Reduces the weight of `Resiable` items, such as backpacks and bedrolls,
to one-quarter the normal value.

