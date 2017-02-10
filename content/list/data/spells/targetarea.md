+++
date = "2016-08-01"
title = "TARGETAREA (Data: spells.lst)"
original_url = "/list/data/spells.html#targetarea"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "TARGETAREA"
    parent = "data_spells"
    identifier = "data_spells_TARGETAREA"
+++

## Status

Updated 6.3.0

## Syntax

`TARGETAREA:x`

## Parameters

-   x: Text (Target area)
-   x: .CLEAR



What it does
------------

-   Reports the Target, Area, or Effects that the spell has.
-   Formulas can be parsed and the results replaced in the output by
    enclosing the variables and formulas within parentheses.
-   [CASTERLEVEL](/list/data/spells/casterlevel.html) , a variable
    specifically designed for this purpose, is commonly used though
    other variables can be used as well.
-   Because anything within parentheses is assumed to be a formula to be
    parsed, text containing parentheses must substitute brackets \[ \]
    in place of parentheses.
-   `.CLEAR` is used to clear the target, area, or effects that a
    spell has.

Example
-------

`TARGETAREA:Cone`

Spell has a cone area of effect.

`TARGETAREA:(CASTERLEVEL*10) ft. cube`

If CASTERLEVEL is equal to 3 then this outputs: "30 ft. cube".

**.MOD Example (Overwriting):**

Initial Spell: `<spell name> <tab> TARGETAREA:(CASTERLEVEL*5) ft. cube`

Modified By:
`<spell name>.MOD <tab> TARGETAREA:(CASTERLEVEL*10) ft. cube`

Is Equivalent To:
`<spell name> <tab> TARGETAREA:(CASTERLEVEL*10) ft. cube`

The target area is now equal to cube 10 times the casterlevel in ft.

