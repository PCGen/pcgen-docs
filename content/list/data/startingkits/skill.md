+++
date = "2016-08-01"
title = "SKILL (Data: starting_kits.lst)"
original_url = "/list/data/startingkits.html#skill"
categories = [ "all-tag", "startingkits-tag" ]
[menu.main]
    name = "SKILL (Data: starting_kits.lst)"
    parent = "startingkits"
+++

## Status

None

## Syntax

`SKILL:x`

## Parameters

-   x: Text (Skill name)
-   x: TYPE=Text (Skill type)



What it does
------------

-   Grants the skill indicated to the character if they can legally have
    that many additional ranks of that skill.
-   The number of ranks granted are determined by the `RANK` tag
    immediately following the `SKILL` tag.
-   `RANK` tag MUST be used on all SKILL lines.
-   If indicated skill is a class skill then ranks will be purchased as
    such, and likewise for cross-class skills.

Examples
--------

`SKILL:Climb RANK:4`

Gives four ranks of "Climb" skill if they can afford it.

`SKILL:TYPE=Knowledge RANK:4`

Gives four ranks of "Knowledge" type skills if they can afford it.

`SKILL:Bluff|Concentration|Hide RANK:18 COUNT:2`

This would offer a chooser and allow you to pick 2 of the three listed
skills and grant 18 ranks to the chosen skills.

