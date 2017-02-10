+++
date = "2016-08-01"
title = "PREPCLEVEL (Global: PRErequisite)"
original_url = "/list/global/pre.html#prepclevel"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREPCLEVEL"
    parent = "global_pre"
+++

## Status

New 5.13.6

## Syntax

`PREPCLEVEL:x,y`

## Parameters

-   x: MIN=Number or formula (Minimum total level).
-   y: MAX=Number or formula (Maximum total level).



What it does
------------

-   Provides the minimum and/or maximum total character class levels the
    character must have to qualify.
-   PREPCLEVEL does not count Monster (Racial) class levels.
-   Class types PC, NPC and Prestige all count as character classes.
-   Either value may be used without the other.

Example
-------

`PREPCLEVEL:MAX=1`

Character must be no greater than 1st level. This can be used to qualify
feats which can only be taken as a 1st level character. A character with
racial hitdice (monster levels) but only 1 or no character class levels
will still qualify.

`PREPCLEVEL:MIN=5`

Character must be at least 5th level.

`PREPCLEVEL:MAX=5`

Character must be no greater than 5th level.

`PREPCLEVEL:MIN=5,MAX=10`

Character must be at least 5th level but no greater than 10th level.

`!PREPCLEVEL:MIN=2,MAX=4`

Character must NOT be 2nd, 3rd or 4th level.

