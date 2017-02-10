+++
date = "2016-08-01"
title = "CRMOD (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#crmod"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "CRMOD"
    parent = "system_gamemode-miscinfo"
+++

## Status

New 6.1.2

## Syntax

`CRMOD:x`

## Parameters

-   x: Formula (a standard PCGen LST formula).



What it does
------------

Specifies the CR reduction mandated by a certain class type. E.g., for
Pathfinder, a character with PC classes has his CRFORMULA value reduced
by 1 after adding up, a character with only NPC classes has his
CRFORMULA formula value reduced by 2 after adding up.

Example
-------

`CRMOD:-1`

CR will be reduces by 1 after all CRFORMULA values are added up.

Where it is used
----------------

CLASSTYPE Line.

