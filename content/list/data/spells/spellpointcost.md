+++
date = "2016-08-01"
title = "SPELLPOINTCOST (Data: spells.lst)"
original_url = "/list/data/spells.html#spellpointcost"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "SPELLPOINTCOST"
    parent = "data_spells"
+++

## Status

New 5.13.x

## Syntax

`SPELLPOINTCOST:x|y=z|y=z`

## Parameters

-   x: Number (Total cost)
-   y: Text (Spell effect)
-   z: Number (Spell effect cost)



What it does
------------

-   This establishes the additional spell point cost for
    spell enhancements.
-   This is a pipe-delimited (|) list of spell effects and spell
    effect costs.

Example
-------

`SPELLPOINTCOST:Evoke Fire=4|Range=1|Area of Effect=1|Duration=1`

Enhancing the "Evoke Fire" effect would cost 4 spell points, the
"Range", "Area of Effect", and "Duration" one point each.

`SPELLPOINTCOST:4`

Enhancing the spell costs a total of 4 spell points.

**.MOD Example (Appending):**

Initial Spell: `<spell name> <tab> SPELLPOINTCOST:Evoke Fire=4`

Modified By: `<spell name>.MOD <tab> SPELLPOINTCOST:Range=1`

Is Equivalent To:
`<spell name> <tab> SPELLPOINTCOST:Evoke Fire=4|Range=1`

Enhancing the "Evoke Fire" effect would cost 4 spell points and the
"Range" one point.

