+++
date = "2016-08-01"
title = "LEVEL (Game Mode: level.lst)"
original_url = "/list/system/gamemode-level.html#level"
categories = [ "all-tag", "gamemode-level-tag" ]
[menu.main]
    name = "LEVEL"
    parent = "system_gamemode-level"
    identifier = "system_gamemode-level_LEVEL"
+++

## Status

None

## Syntax

`
LEVEL:x`

## Parameters

-   x: Number (Level)
-   x: LEVEL



What it does
------------

-   Determines level based benefits.
-   Using `LEVEL` in conjunction with a formula on the `MINXP` tag that
    utilizes the <span class="lstvar"> LEVEL </span> variable will
    determine the level benefits.

Example
-------

`LEVEL:1 <tab> MINXP:0 <tab> CSKILLMAX:1 <tab> CCSKILLMAX:1`

Identifies the minimum experience points amd maximum class and
cross-class skill ranks for first level.

`LEVEL:LEVEL <tab> MINXP:(LEVEL*LEVEL-LEVEL)*500 <tab> CSKILLMAX:LEVEL+3 <tab> CCSKILLMAX:(LEVEL+3)/2`

Establishes the standard level progression by experience points as used
in the R/SRD.

