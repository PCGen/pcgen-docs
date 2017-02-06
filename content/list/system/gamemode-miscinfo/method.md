+++
date = "2016-08-01"
title = "METHOD (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#method"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "METHOD (Game Mode: miscinfo.lst)"
    parent = "gamemode-miscinfo"
+++

## Status

New 5.9.3

## Syntax

`METHOD:x`

## Parameters

-   x: Formula (Random Stat rolling method formula).



What it does
------------

Follows a [ROLLMETHOD](/list/system/gamemode-miscinfo/rollmethod.html)
tag and defines the dice formula used.

Example
-------

`ROLLMETHOD:3d6 <tab> METHOD:3d6`

Menu displays "3d6" as the label for this method and simulates rolling 3
six sided dice.

`ROLLMETHOD:4d6 drop lowest <tab> METHOD:roll(4,6,[2,3,4])`

Simulates rolling 4 six sided dice and dropping the lowest.

`ROLLMETHOD:5d6 drop 2 lowest <tab> METHOD:roll(5,6,[3,4,5])`

Simulates rolling 5 six sided dice and dropping the 2 lowest.

`ROLLMETHOD:4d6 drop lowest <tab> METHOD:roll(4,6,top(3))`

Simulates rolling 4 six sided dice and dropping the lowest.

`ROLLMETHOD:4d6, reroll 1's, drop the lowest <tab> METHOD:roll(4,6,top(3),reroll(1))`

Simulates rolling 4 six sided dice, rerolling 1's and dropping the
lowest.

`ROLLMETHOD:5d6, reroll 1&2's, drop 2 lowest <tab> METHOD:roll(5,6,top(3), reroll(2))`

Simulates rolling 5 six sided dice, rerolling any 1's and 2's and
dropping the 2 lowest.

**Where is this used:**

In a [ROLLMETHOD](/list/system/gamemode-miscinfo/rollmethod.html) line.

