+++
date = "2016-08-01"
title = "SKILLPOOL (Global: BONUS)"
original_url = "/list/global/bonus.html#skillpool"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "SKILLPOOL"
    parent = "global_bonus"
    identifier = "global_bonus_SKILLPOOL"
+++

## Status

New 5.3.9

## Syntax

`BONUS:SKILLPOOL|CLASS=x;LEVEL=y|z`

## Parameters

-   x: Text (Class the points are to be awarded to)
-   y: Number (Class Level the points are to be
    awarded to)
-   z: Number (Number of points to be added to skill
    the pool)



What it Does
------------

Adds to the number of points in the skill pool of the class at the level
specified.

Examples
--------

`BONUS:SKILLPOOL|CLASS=Fighter;LEVEL=2|2`

Adds 2 additional skillpoints to the character's skill pool at the
second level of the character's Fighter Class.

`BONUS:SKILLPOOL|CLASS=Wizard;LEVEL=5|4|PRESTAT:1,INT=18`

Adds 4 additional skillpoints to the character's skill pool at the fifth
level of the character's Wizard Class if he has an intelligence of 18 or
better.

