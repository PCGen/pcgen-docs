+++
date = "2016-08-01"
title = "PREEQUIPTWOWEAPON (Global: PRErequisite)"
original_url = "/list/global/pre.html#preequiptwoweapon"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREEQUIPTWOWEAPON"
    parent = "global_pre"
+++

## Status

None

## Syntax

`PREEQUIPTWOWEAPON:x,y,y`

## Parameters

-   x: Number (The number of items that must be
    equipped in a two weapon fighting manner - 1 or 2).
-   y: Text (Weapon name - "%" may be used as
    a wildcard)
-   y: TYPE=Text (Weapon type)
-   y: WIELDCATEGORY=Text (Wield category).



What it does
------------

This is used to determine if a character has a particular item (usually
a weapon) equipped and used two weapon style.

Examples
--------

`PREEQUIPTWOWEAPON:1,Sword (Short)`

Must have a Sword (Short) equipped as one of two weapons for two weapon
fighting.

`PREEQUIPTWOWEAPON:1,Sword (Short%`

Must have a Sword (Short) equipped as one of two weapons and allows for
items named Sword (Short/Masterwork) etc.

`PREEQUIPTWOWEAPON:1,TYPE=Slashing`

Must have a "Slashing" type weapon equipped as one of two weapons for
two weapon fighting.

`PREEQUIPTWOWEAPON:1,WIELDCATEGORY=Light`

Must have a light weapon equipped for two weapon fighting.

