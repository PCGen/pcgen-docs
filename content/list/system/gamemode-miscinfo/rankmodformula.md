+++
date = "2016-08-01"
title = "RANKMODFORMULA (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#rankmodformula"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "RANKMODFORMULA (Game Mode: miscinfo.lst)"
    parent = "gamemode-miscinfo"
+++

## Status

New 5.8.0

## Syntax

`RANKMODFORMULA:x`

## Parameters

-   x: Formula (Formula to calculate skill bonus)



What it does
------------

-   The RANKMODFORMULA tag is used to set the bonus to a skills total
    that each rank in the skill gives.
-   The formula can use any valid JEP expressions.
-   The formula can reference any variables defined for the character.
-   The token \$\$RANK\$\$ will be replaced with the skills total ranks.

Example
-------

`RANKMODFORMULA:IF($$RANK$$>20,50+$$RANK$$,IF($$RANK$$>10,50+($$RANK$$-10)*2,IF($$RANK$$>0,$$RANK$$*5,-25)))-$$RANK$$`

The first 10 ranks of a skill will each give +5 bonus to the skill
total. The next 10 give a +2 bonus and any additional ranks give a +1
bonus to skill total. A skill without ranks has a bonus of -25. (This is
HARP's skill point system.)

