+++
date = "2016-08-01"
title = "COST (Data: spells.lst)"
original_url = "/list/data/spells.html#cost"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "COST"
    parent = "data_spells"
+++

## Status

Updated 6.3.0

## Syntax

`COST:x`

## Parameters

-   x: Number (Component Cost)
-   x: .CLEAR



What it does
------------

-   This tag identifies the cost of the spell's components.
-   `.CLEAR` is used to clear the cost of a spell's components.

Example
-------

`COST:300`

**.MOD Example (Overwriting):**

Initial Spell: `<spell name> <tab> COST:300`

Modified By: `<spell name>.MOD <tab> COST:150`

Is Equivalent To: `<spell name> <tab> COST:150`

The associated spell components cost 150 gp.

