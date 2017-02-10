+++
date = "2016-08-01"
title = "PREEQUIPBOTH (Global: PRErequisite)"
original_url = "/list/global/pre.html#preequipboth"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREEQUIPBOTH"
    parent = "global_pre"
    identifier = "global_pre_PREEQUIPBOTH"
+++

## Status

None

## Syntax

`PREEQUIPBOTH:x,y`

## Parameters

-   x: Number (Number of items to be equipped).
-   y: Text (Equipment name).
-   y: TYPE=Text (Equipment type).
-   y: WIELDCATEGORY=Text (Wield category name).



What it does
------------

This is used to determine if a character has a particular item (usually
a weapon) equipped and used two-handed style.

Examples
--------

`PREEQUIPBOTH:1,Quarterstaff`

Must have a Quarterstaff equipped in both hands.

`PREEQUIPBOTH:1,Sword (Great%`

The "%" allows for items named Sword (Great/Masterwork) etc.

`PREEQUIPBOTH:1,TYPE=Slashing`

Must have a slashing type weapon equipped in both hands.

