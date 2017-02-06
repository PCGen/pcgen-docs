+++
date = "2016-08-01"
title = "PRESA (Global: PRErequisite)"
original_url = "/list/global/pre.html#presa"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRESA (Global: PRErequisite)"
    parent = "pre"
+++

## Status

None

## Syntax

`PRESA:x,y,y`

## Parameters

-   x: Number (The number of Special Abilities a
    character must have).
-   y: Text (The name of an Special Abilities).



What it does
------------

-   Checks for the specified special abilities as a prerequisite.
-   Special abilities applied by the `SAB` tag will satisfy
    this prerequisite.

Example
-------

`PRESA:1,Turn undead,Rebuke undead,Smite Evil`

Character must have any one of "Turn Undead", "Rebuke Undead" or "Smite
Evil".

`CLASS:Mystic Theurge.MOD <tab> !PRESA:1,Theurgy`

Character must not have any Special Abilities of "Theurgy".

