+++
date = "2016-08-01"
title = "BONUSACVALUE (System: sizeAdjustment.lst)"
original_url = "list/system/sizeadjustment.html#bonusacvalue"
categories = [ "all-tag", "sizeadjustment-tag" ]
+++

## Status

None

## Syntax

`None`

## Parameters




<span id="bonusacvalue"></span>

### BONUS:ACVALUE

Multiplies the AC bonus from a particular type of armour, such as
`Armor` or `Shield` , based on the creature's size.

Only works in `sizeAdjustment.lst`.

#### Status {#status-2}

New in 5.10.1.

#### Syntax {#syntax-4}

`BONUS:ACVALUE|TYPE:type_1,TYPE:type_2, ...|ac_multiplier`

-   `type_1` , `type_2` , ... may include armour types such as
    `TYPE:Armor` and `TYPE:Shield` .
    -   *\[Ed: do things like `TYPE:Natural` , `TYPE:Dodge` ,
        `TYPE:Sacred` ... also work?\]*
-   `ac_multiplier` is the multiplier to AC for the given armour types.
    -   `0.5` would cause the creature to only receive half the normal
        AC bonus from the given armour types.
    -   `2` would cause the creature to gain twice the AC bonus from the
        given armour types.

#### Examples

-   `BONUS:ACVALUE|TYPE.Armor,TYPE.Shield|0.5`

Halves the benefit from armour and shields.

-   `BONUS:ACVALUE|TYPE.Armor,TYPE.Shield|2`

Doubles the benefit from armour and shields.

