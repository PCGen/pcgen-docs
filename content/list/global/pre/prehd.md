+++
date = "2016-08-01"
title = "PREHD (Global: PRErequisite)"
original_url = "/list/global/pre.html#prehd"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREHD"
    parent = "global_pre"
+++

## Status

Updated 5.13.5

## Syntax

`PREHD:x,y`

## Parameters

-   x: MIN=Number or Formula (Minimum racial Hit Dice)
-   y: MAX=Number or Formula (Maximum racial Hit Dice)



What it does
------------

-   Provides the number, minimum or maximum, of hit dice the character
    must have to qualify.
-   This test looks at a character's racial HD and/or any levels of
    Monster Classes only.

Examples
--------

`PREHD:MIN=1,MAX=3`

The character must have one, two, or three racial hit die monster
levels.

`PREHD:MIN=4`

The character must have four or more racial hit die or monster levels.

`PREHD:MAX=4`

The character must have four or fewer racial hit die monster levels.

`!PREHD:MIN=5,MAX=7`

Character must have between 0-4 OR 7 or greater racial hit die or
monster levels.

