+++
date = "2016-08-01"
title = "SKILLMULTIPLIER (Game Mode: miscinfo.lst)"
original_url = "list/system/gamemode-miscinfo.html#skillmultiplier"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
+++

## Status

None

## Syntax

`SKILLMULTIPLIER:x|x`

## Parameters

-   x: Number (The skill multiplier for the level -
    level is based on position).



What it does
------------

-   Alters the number of skill points awarded at various levels
    of advancement.
-   Currently implemented to support the standard rule that characters
    get 4x the normal amount of skills at first level.

Examples
--------

`SKILLMULTIPLIER:4`

Character gets 4x the normal amount of skills, at 1st level.

`SKILLMULTIPLIER:2|2|2`

Character gets 2x the normal amount of skills, at 1st, 2nd, and 3rd
level.

`SKILLMULTIPLIER:10|4`

Character get 10x the normal amount of skills at 1st level and 4x the
normal amount of skills at 2nd level.

