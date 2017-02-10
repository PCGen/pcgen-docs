+++
date = "2016-08-01"
title = "PRELEVEL (Global: PRErequisite)"
original_url = "/list/global/pre.html#prelevel"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRELEVEL"
    parent = "global_pre"
    identifier = "global_pre_PRELEVEL"
+++

## Status

Updated 5.13.5

## Syntax

`PRELEVEL:x,y`

## Parameters

-   x: MIN=Number or formula (Minimum total level).
-   y: MAX=Number or formula (Maximum total level).



What it does
------------

-   Provides the minimum and/or maximum total levels, including all
    character, racial, or monster class levels, the character must have
    to qualify.
-   Either value may be used without the other.

Example
-------

`PRELEVEL:MIN=5`

Character must be at least 5th level.

`PRELEVEL:MAX=5`

Character must be no greater than 5th level.

`PRELEVEL:MIN=5,MAX=10`

Character must be at least 5th level but no greater than 10th level.

`!PRELEVEL:MIN=3,MAX=6`

Character must NOT be 3rd, 4th, 5th or 6th level.

