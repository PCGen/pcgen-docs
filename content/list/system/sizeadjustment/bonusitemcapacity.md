+++
date = "2016-08-01"
title = "BONUSITEMCAPACITY (System: sizeAdjustment.lst)"
original_url = "/list/system/sizeadjustment.html#bonusitemcapacity"
categories = [ "all-tag", "sizeadjustment-tag" ]
[menu.main]
    name = "BONUSITEMCAPACITY (System: sizeAdjustment.lst)"
    parent = "sizeadjustment"
+++

## Status

None

## Syntax

`None`

## Parameters




<span id="bonusitemcapacity"></span>

### BONUS:ITEMCAPACITY

Changes the "item carrying capacity" based on the size of the character.

This is used to implement the DnD 3.5 rule for equipment made in
different sizes for different creatures, such as backpacks and
bed-rolls. These items *"... weigh one-quarter this amount when made for
Small characters. Containers for Small characters also **carry
one-quarter the normal amount.** "* ( [Refer to the d20
SRD.](http://www.d20srd.org/srd/equipment/goodsAndServices.htm#adventuringGear)
)

Only works in `sizeAdjustment.lst`.

#### Status {#status-3}

New in 5.10.1

#### Syntax {#syntax-5}

`BONUS:ITEMCAPACITY|TYPE=item_type|capacity_multiplier`

-   `item_type` is a type of equipment from the data set's equipment
    files, i.e. the `35e` files `rsrd_equip_arms_and_armor.lst` ,
    `rsrd_equip_general.lst` , and `rsrd_equip_magic_items.lst` . Such
    types might include:
-   `Resizable` - for items which are [supposed to come in different
    sizes for different
    characters](http://www.d20srd.org/srd/equipment/goodsAndServices.htm#adventuringGear)
    , like backpacks, blankets, bedrolls, and so on.
-   `Goods` - seems to include the majority of things in the
    `rsrd_equip_general.lst` , which covers general [goods and
    services](http://www.d20srd.org/srd/equipment/goodsAndServices.htm#adventuringGear) .

-   `capacity_multiplier` is a number.

#### Examples {#examples-1}

-   `BONUS:ITEMCAPACITY|TYPE=Resizable|0.25`

Reduces the carrying capacity of items of `TYPE=Resizable` to one
quarter of the normal value.

-   `BONUS:ITEMCAPACITY|TYPE=Goods|2`

Increases the carrying capacity of `TYPE=Goods` to double the normal
value.

