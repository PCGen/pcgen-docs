+++
date = "2016-08-01"
title = "DURATION (Data: spells.lst)"
original_url = "/list/data/spells.html#duration"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "DURATION"
    parent = "data_spells"
+++

## Status

None

## Syntax

`DURATION:x`

## Parameters

-   x: Text (Spell duration)



What it does
------------

-   Reports the duration of the spell.
-   Formulas can be parsed and the results replaced in the output by
    enclosing the variables and formulas within parentheses.
-   [CASTERLEVEL](/list/data/spells/casterlevel.html) , a variable
    specifically designed for this purpose, is commonly used though
    other variables can be used as well.
-   Because anything within parentheses is assumed to be a formula to be
    parsed, text containing parentheses must substitute brackets \[ \]
    in place of parentheses.

Example
-------

`DURATION:1 Round/Level`

This spell lasts for one round per level.

`DURATION:(CASTERLEVEL) rounds`

If CASTERLEVEL is equal to 3 then this outputs: "3 rounds".

**.MOD Example (Appending):**

Initial Spell: `<spell name> <tab> DURATION:1 Round/Level`

Modified By: `<spell name>.MOD <tab> DURATION:(CASTERLEVEL) rounds`

Is Equivalent To:
`<spell name> <tab> DURATION:1 Round/Level|(CASTERLEVEL) rounds`

For a 3rd level spellcaster the associated spell appears on the output
sheet with a duration of "1 Round/Level, 3 rounds".

