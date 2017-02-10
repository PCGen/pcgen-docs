+++
date = "2016-08-01"
title = "CASTTIME (Data: spells.lst)"
original_url = "/list/data/spells.html#casttime"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "CASTTIME"
    parent = "data_spells"
+++

## Status

None

## Syntax

`CASTTIME:x`

## Parameters

-   x: Text (Casting time)



What it does
------------

Reports the time it takes to cast this spell.

Example
-------

`CASTTIME:1 Round`

This spell takes 1 round to cast.

**.MOD Example (Appending):**

Initial Spell: `<spell name> <tab> CASTTIME:1 Round`

Modified By: `<spell name>.MOD <tab> CASTTIME:10 Minute Ritual`

Is Equivalent To: `<spell name> <tab> CASTTIME:1 Round|10 Minute Ritual`

The output sheet will display "1 Round, 10 Minute Ritual" on the output
sheet.

