+++
date = "2016-08-01"
title = "POOL (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#pool"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "POOL"
    parent = "system_gamemode-miscinfo"
+++

## Status

New 5.11.1

## Syntax

`POOL:x`

## Parameters

-   x: Number, Variable, or Formula (Ability
    pool value)



What it does
------------

-   Used in
    [ABILITYCATEGORY](/list/system/gamemode-miscinfo/abilitycategory.html)
    lines to establish the number, variable, or formula to use to
    calculate the pool size for this category of ability.
-   If a variable is used it **MUST** be defined using the `DEFINE` tag.

Example
-------

`POOL:TL/2`

The ability pool equals a value equal to that of half the character's
total level.

Where it is used
----------------

Used in
[ABILITYCATEGORY](/list/system/gamemode-miscinfo/abilitycategory.html)
lines in the *miscinfo.lst* and *abilitycategory.lst* files.

