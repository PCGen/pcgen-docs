+++
date = "2016-08-01"
title = "RANK (Data: starting_kits.lst)"
original_url = "list/data/startingkits.html#rank"
categories = [ "all-tag", "startingkits-tag" ]
+++

## Status

None

## Syntax

`RANK:x`

## Parameters

-   x: Number (Skill rank)



What it does
------------

-   Grants the number of ranks to the skill indicated, in the
    immediately preceeding `SKILL` tag, to the character if they can
    legally have that many additional ranks of that skill.
-   `RANK` tag MUST be used on all SKILL lines.
-   If the indicated skill is a class skill then ranks will be purchased
    as such, and likewise for cross-class skills.

Examples
--------

`SKILL:Climb RANK:4`

Gives four ranks of "Climb" skill if they can afford it.

`SKILL:TYPE=Knowledge RANK:4`

Gives four ranks of "Knowledge" type skills if they can afford it.

Where it is Used
----------------

SKILL line

