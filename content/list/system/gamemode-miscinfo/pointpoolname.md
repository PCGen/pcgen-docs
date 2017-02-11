+++
date = "2016-08-01"
title = "POINTPOOLNAME (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#pointpoolname"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "POINTPOOLNAME"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_POINTPOOLNAME"
+++

## Status

None

## Syntax

`POINTPOOLNAME:x`

## Parameters

-   x: Text (Pointbuy Method Name)



What it does
------------

-   The `POINTPOOLNAME` tag is used to make a default choice for a
    GameMode's preferred method of PointPooling for Stat creation.
-   The pointbuy method referenced must have a matching entry in the
    GameMode's <span class="lstfile"> pointbuymethod.lst </span> file.
-   When the `POINTPOOLNAME` tag is present in the <span
    class="lstfile"> miscinfo.lst </span> file:
    -   The Summary Tab will display total points/points remaining (i.e.
        Development Points 160/135) on the same line as the stat total
        and stat mod total
    -   The Skills Tab displays the pool of availble skill points to
        spend instead of skill points by class/level requirement, and is
        populated by the classes `STARTSKILLPTS` and miscinfo
        `SKILLMULTIPLIER`
    -   The Feats Tab will show total point pool as described for the
        skills tab.

Example
-------

`POINTPOOLNAME:Harp`

Means that PCGen will use the Harp Point Pool default for stat creation.

