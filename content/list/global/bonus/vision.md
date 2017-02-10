+++
date = "2016-08-01"
title = "VISION (Global: BONUS)"
original_url = "/list/global/bonus.html#vision"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "VISION"
    parent = "global_bonus"
    identifier = "global_bonus_VISION"
+++

## Status

New 5.5.5

## Syntax

`BONUS:VISION|x|y`

## Parameters

-   x: Text (Vision type)
-   y: Number, variable or formula (Number or formula
    to adjust vision range by)



What it Does
------------

-   Adds the vision type specified if you don't already have it,
    otherwise it increases the range of the vision type by the
    number specified.
-   Vision types include (but are not limited to): Blindsense,
    Darkvision, Low-Light.

Example
-------

`BONUS:VISION|Darkvision|30`

Adds DarkVision (30') if you don't have Darkvision, otherwise it
increases your darkvision range by 30'.

`BONUS:VISION|Darkvision|((CL/4).TRUNC+1)*10`

Increases a character's Darkvision by 10 feet every four levels starting
at 1st level.

`BONUS:VISION|Darkvision|60|PRERACE:1,TYPE=Robot`

Adds Darkvision (60') if you don't have Darkvision, otherwise it
increases your darkvision range by 60', if you are a robot.

