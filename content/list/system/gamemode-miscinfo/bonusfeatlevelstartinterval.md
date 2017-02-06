+++
date = "2016-08-01"
title = "BONUSFEATLEVELSTARTINTERVAL (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#bonusfeatlevelstartinterval"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "BONUSFEATLEVELSTARTINTERVAL (Game Mode: miscinfo.lst)"
    parent = "gamemode-miscinfo"
+++

## Status

None

## Syntax

`BONUSFEATLEVELSTARTINTERVAL:x|y`

## Parameters

-   x: Number (Level where bonus feats would begin
    (first bonus feat awarded at this level).
-   y: Number (Level increment to get more feats - e.g.
    3 for every third level).



What it does
------------

-   This tag, basically, sets the feat progression rules.
-   Where level = first level where you gain an additional feat (use
    more than one of these tags for additional feat progressions).
-   Where interval = multiples of levels after the start level that you
    gain an additional feat (0 = only at start).
-   The standard setting would give characters get a bonus feat every
    three levels starting at level three, so the tag info would be 3|3
    (1st three indicates that the first bonus feat is given at level 3,
    and the 2nd three indicates that additional bonus feats are given
    every three levels after that).

Example
-------

`BONUSFEATLEVELSTARTINTERVAL:1|0`

Character would get one bonus feat at creation and never again after
that.

`BONUSFEATLEVELSTARTINTERVAL:3|3`

Character would get a bonus feat every three levels, starting at level
3.

`BONUSFEATLEVELSTARTINTERVAL:2|3`

Character would get a bonus feat every three levels, starting at level
2.

