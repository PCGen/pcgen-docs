+++
date = "2016-08-01"
title = "MOVEADD (Global: BONUS)"
original_url = "/list/global/bonus.html#moveadd"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "MOVEADD"
    parent = "global_bonus"
    identifier = "global_bonus_MOVEADD"
+++

## Status

New 4.3.8

## Syntax

`BONUS:MOVEADD|x|y`

## Parameters

-   x: TYPE.Text (Movement type)
-   x: TYPE.All
-   y: Number, variable or formula (Number to add to
    movement rate)



What it Does
------------

-   Adds to movement of the listed type.
-   Done before `MOVEMULT` and `POSTMOVEADD` calculations.
-   It only works on MOVE types that have been defined in a `MOVE` or
    `MOVECLONE` tag.

Examples
--------

`BONUS:MOVEADD|TYPE.Walk|10`

Adds 10 to Walk.

`BONUS:MOVEADD|TYPE.Walk|5|PREVARLT:ENCUMBERANCE,1`

Adds 5 to Walk so long as the character is not at medium load.

`TEMPBONUS:ANYPC|MOVEADD|TYPE.Walk|10|TYPE=Enhancement`

Adds 5 to the character's Walk as an enhancement of some sort.

