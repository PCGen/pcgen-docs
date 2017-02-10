+++
date = "2016-08-01"
title = "XPCOST (Data: spells.lst)"
original_url = "/list/data/spells.html#xpcost"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "XPCOST"
    parent = "data_spells"
    identifier = "data_spells_XPCOST"
+++

## Status

None

## Syntax

`XPCOST:x`

## Parameters

-   x: Number (Spell XP Cost)



What it does
------------

Denotes how much the spell costs to cast, used for determining potion,
wand, etc costs.

XPCOST must be an integer &gt;= 0

Example
-------

`XPCOST:1250`

Spell costs 1250 Experience points to cast.

**.MOD Example (Overwriting):**

Initial Spell: `<spell name> <tab> XPCOST:1250`

Modified By: `<spell name>.MOD <tab> XPCOST:750`

Is Equivalent To: `<spell name> <tab> XPCOST:750`

Spell costs 750 Experience points to cast.

