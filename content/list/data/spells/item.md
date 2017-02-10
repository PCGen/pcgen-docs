+++
date = "2016-08-01"
title = "ITEM (Data: spells.lst)"
original_url = "/list/data/spells.html#item"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "ITEM"
    parent = "data_spells"
    identifier = "data_spells_ITEM"
+++

## Status

Updated before 5.12.0

## Syntax

`ITEM:x`

## Parameters

-   x: Text (Item type)



What it does
------------

Tells PCGen what types of items this spell can be used to make (Potions,
wands, wondrous items, etc).

Most often this is used to indicate the spell can be made into a potion.

Brackets can be used to prevent the spell from being used in the
specified item.

Example
-------

`ITEM:Potion`

This spell can be used in a potion.

`ITEM:[Scroll]`

This spell can NOT be used in a scroll.

**.MOD Example (Appending):**

Initial Spell: `<spell name> <tab> ITEM:Scroll`

Modified By: `<spell name>.MOD <tab> ITEM:Potion`

Is Equivalent To: `<spell name> <tab> ITEM:Scroll|Potion`

The associated spell can be used to make scrolls and potions.

