+++
date = "2016-08-01"
title = "MODIFIER (Game Mode: load.lst"
original_url = "/list/system/gamemode-load.html#modifier"
categories = [ "all-tag", "gamemode-load-tag" ]
[menu.main]
    name = "MODIFIER (Game Mode: load.lst"
    parent = "system_gamemode-load"
    identifier = "system_gamemode-load_MODIFIER (Game Mode: load.lst"
+++

## Status

None

## Syntax

`MODIFIER:x`

## Parameters

-   x: Number, Variable or Formula



What it does
------------

-   Provides the maximum load value.
-   This tag is optional. If not included, the maximum load is the
    internally generated \$\$SCORE\$\$.

Example
-------

`MODIFIER:$$SCORE$$*(1+EquipLoadBonusMult)`\

The load score, \$\$SCORE\$\$, is modified by a multiplier of
EquipLoadBonusMult+1.

