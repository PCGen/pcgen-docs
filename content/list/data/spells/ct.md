+++
date = "2016-08-01"
title = "CT (Data: spells.lst)"
original_url = "/list/data/spells.html#ct"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "CT"
    parent = "data_spells"
    identifier = "data_spells_CT"
+++

## Status

New 5.11.6

## Syntax

`CT:x`

## Parameters

-   x: Number (Casting Threshold)



What it does
------------

-   This roll is applied/accumulated toward the Casting Threshold of the
    spell that the mage is casting.
-   `CT` must be in integer &gt;= 0

Example
-------

`CT:41`

This spell takes 41+ points to cast.

**.MOD Example (Overwriting):**

Initial Spell: `<spell name> <tab> CT:25`

Modified By: `<spell name>.MOD <tab> CT:35`

Is Equivalent To: `<spell name> <tab> CT:35`

The casting threshold of the associated spell is 35.

