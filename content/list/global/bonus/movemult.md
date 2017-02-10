+++
date = "2016-08-01"
title = "MOVEMULT (Global: BONUS)"
original_url = "/list/global/bonus.html#movemult"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "MOVEMULT"
    parent = "global_bonus"
+++

## Status

New 4.3.8

## Syntax

`BONUS:MOVEMULT|x|y`

## Parameters

-   x: TYPE.Text (Movement type)
-   x: TYPE.All
-   y: Number, variable or formula (Number to multiply
    the movement rate)



What it Does
------------

-   Multiplies the movement of the listed TYPEs.
-   Done before `MOVEMULT` and `POSTMOVEADD` calculations.
-   It only works on MOVE types that have been defined in a `MOVE` or
    `MOVECLONE` tag.

Note: PCGen does not use both `BONUS:MOVEMULT` and `BONUS:POSTMOVEADD`
in calculating the total move adjustment. The total move adjustment is
set to the greatest value between (Base Move + POSTMOVEADD) and (Base
Move x MOVEMULT).

Example
-------

`BONUS:MOVEMULT|TYPE.Walk,TYPE.Fly|2`

Multiplies the Walk & Fly movement rates by two.

`BONUS:MOVEMULT|TYPE=Walk,TYPE=Fly,TYPE=Climb,TYPE=Hover,TYPE=Swim|2`

Multiplies the Walk, Fly, Climb, Hover, Swim movement rates by two.

