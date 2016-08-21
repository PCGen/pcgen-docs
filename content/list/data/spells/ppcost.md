+++
date = "2016-08-01"
title = "PPCOST (Data: spells.lst)"
original_url = "list/data/spells.html#ppcost"
categories = [ "all-tag", "spells-tag" ]
+++

## Status

NEW 5.10.1

## Syntax

`PPCOST:x`

## Parameters

-   x: Number



What it does
------------

This is a point pool cost to purchase/cast the spell works with
SKILLTOTAL=&gt;skill name)

Example
-------

`PPCOST:9`

This spell costs 9 points to use.

**.MOD Example (Overwriting):**

Initial Spell: `<spell name> <tab> PPCOST:3`

Modified By: `<spell name>.MOD <tab> PPCOST:6`

Is Equivalent To: `<spell name> <tab> PPCOST:6`

The associated spells costs "6" power points.

