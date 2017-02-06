+++
date = "2016-08-01"
title = "RANGE (Data: spells.lst)"
original_url = "/list/data/spells.html#range"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "RANGE (Data: spells.lst)"
    parent = "spells"
+++

## Status

Updated 5.13.6

## Syntax

`RANGE:x`

## Parameters

-   x: Text (Spell range)



What it does
------------

Reports the range that the spell has.

Example
-------

`RANGE:Medium (100' + 5/lv)`

This spell has a range of 100 feet plus 5 feet per level.

`RANGE:.CLEAR <tab> RANGE:Personal`

This clears the previous range and replaces with "Personal" range.

**.MOD Example (Appending):**

Initial Spell: `<spell name> <tab> RANGE:Personal`

Modified By: `<spell name>.MOD <tab> RANGE:Medium (100' + 5/lvl)`

Is Equivalent To:
`<spell name> <tab> RANGE:Personal|Medium (100' + 5/lvl)`

The associated spell can be used as a personal spell or at medium range.

