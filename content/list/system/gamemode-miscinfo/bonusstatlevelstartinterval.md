+++
date = "2016-08-01"
title = "BONUSSTATLEVELSTARTINTERVAL (Game Mode: miscinfo.lst)"
original_url = "list/system/gamemode-miscinfo.html#bonusstatlevelstartinterval"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
+++

## Status

Updated 5.15.0

## Syntax

`BONUSSTATLEVELSTARTINTERVAL:x|y|x`

## Parameters

-   x: Number (Begining Level)
-   y: Number or Formula (Level Interval)
-   z: Number (Number of Stats, Optional)



What it does
------------

-   This tag sets the stat progression rules.
    -   Beginning level (x) is the first level where you gain an
        additional stat (use more than one of these tags for additional
        stat progressions).
    -   Level Interval (y) defines the interval levels after the start
        level that you gain an additional stat bonus. Setting this
        parameter to zero (0) will limit bonus stat increases to the
        beginning level.
    -   Number of Stats (z) defines the number of stats that can be
        increases at each level where bonusas are allowed. This
        parameter is optional and will default to "1" if not
        otherwise defned.
-   The standard setting would give characters a bonus stat point every
    four levels starting at level four, so the tag info would be 4|4
    (1st four indicates that the first bonus stat point is given at
    level 4, and the 2nd four indicates that additional bonus stat
    points are given every four levels after that).

Example
-------

`BONUSSTATLEVELSTARTINTERVAL:1|0`

Character would get a bonus stat point at 1st with no bonuses after
that.

`BONUSSTATLEVELSTARTINTERVAL:4|4`

Character would get a bonus stat point at 4th level with an additional
stat boint every four levels after that. (e.g. 4,8,12,16, 20)

`BONUSSTATLEVELSTARTINTERVAL:2|3`

Character would get a bonus stat point every three levels, starting at
level 2.

`BONUSSTATLEVELSTARTINTERVAL:4|0|3`

Character would get 3 bonus stat points at fourth level with no binuses
after that.

`BONUSSTATLEVELSTARTINTERVAL:4|if(mod(TL,10)>0&&mod(mod(TL,10),4)==0,1,0)|2`

Character would get bonus 2 stat points at 4th level and at every
interval determined by the formula provided. (e.g. 4, 8, 14, 18, 24, 28)

