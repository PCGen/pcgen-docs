+++
date = "2016-08-01"
title = "POSTMOVEADD (Global: BONUS)"
original_url = "/list/global/bonus.html#postmoveadd"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "POSTMOVEADD (Global: BONUS)"
    parent = "bonus"
+++

## Status

New 4.3.8

## Syntax

` BONUS:POSTMOVEADD|x|y`

## Parameters

-   x: TYPE.Text (Movement type)
-   x: TYPE.All
-   y: Number, variable or formula (Number to add to
    movement rate)



What it Does
------------

-   This tag will increase the movement of the listed types.
-   Done after `MOVEMULT` and `MOVEADD` calculations.
-   It only works on MOVE types that have been defined in a `MOVE` or
    `MOVECLONE` tag.

Note: PCGen does not use both `BONUS:MOVEMULT` and `BONUS:POSTMOVEADD`
in calculating the total move adjustment. The total move adjustment is
set to the greatest value between (Base Move + POSTMOVEADD) and (Base
Move x MOVEMULT).

Example
-------

`BONUS:POSTMOVEADD|TYPE.Walk|10`

Adds 10 to Walk.

`TEMPBONUS:PC|POSTMOVEADD|TYPE.Walk,TYPE.Burrow,TYPE.Climb,TYPE.Fly,TYPE.Swim|30|TYPE=Enhancement`

Adds 30 to Walk, Burrow, Climb, Fly and Swim to any PC Character that
has this enhancement.

