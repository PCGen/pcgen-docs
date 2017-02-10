+++
date = "2016-08-01"
title = "BONUSLANG (Game Mode: statsandchecks.lst)"
original_url = "/list/system/gamemode-statsandchecks.html#bonuslang"
categories = [ "all-tag", "gamemode-statsandchecks-tag" ]
[menu.main]
    name = "BONUSLANG"
    parent = "system_gamemode-statsandchecks"
    identifier = "system_gamemode-statsandchecks_BONUSLANG"
+++

## Status

New 5.10.1

## Syntax

`BONUS:LANG|x|y`

## Parameters

-   x: defined variable
-   y: Number, variable or formula



What it does
------------

Adds to defined varaibles

Example
-------

`BONUS:LANG|BONUS|INT`

Adds the value of INT modifier to total the defined variable and
language skill, as defined in miscinfo.lst and else where.

Where it is used
----------------

STATNAME Line.

