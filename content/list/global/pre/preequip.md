+++
date = "2016-08-01"
title = "PREEQUIP (Global: PRErequisite)"
original_url = "list/global/pre.html#preequip"
categories = [ "all-tag", "pre-tag" ]
+++

## Status

None

## Syntax

`PREEQUIP:x,y,y`

## Parameters

-   x: Number (The number of items to be equipped)
-   y: Text (Equipment name)
-   y: TYPE=Text (Equipment type)
-   y: WIELDCATEGORY=Text (Wield category of a weapon)



What it does
------------

-   This is used to determine if a character has a particular item(s)
    equipped.
-   The percent symbol (%) may be used as a wild-card when including
    text in the list of parameters.
-   Multiple TYPEs may be stacked by including them in a period
    delimited (.) list. (e.g. TYPE=Heavy.Armor for "Heavy Armor")

Examples
--------

`PREEQUIP:1,Leather Armor`

Must have Leather Armor (only) equipped.

`PREEQUIP:1,Leather Armor%`

The "%" allows for items named Leather Armor (Masterwork), Leather Armor
(+1) etc.

`PREEQUIP:1,TYPE=Armor`

Must have some type of armor equipped.

`PREEQUIP:2,TYPE=Armor,Sword (Long)%`

Must be equipped with any Sword (Long), as well as any type of armor.

`PREEQUIP:2,TYPE=Armor,TYPE=Shield`

Must be equipped with any Armor and any Shield.

`PREEQUIP:1,WIELDCATEGORY=TwoHanded`

Must be equipped with a two handed weapon.

`PREEQUIP:1,TYPE=Armor.Heavy,TYPE=Armor.Light`

Must have equipped Heavy Armor or Light Armor.

