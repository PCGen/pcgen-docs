+++
date = "2016-08-01"
title = "WEAPONREACH (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#weaponreach"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "WEAPONREACH"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_WEAPONREACH"
+++

## Status

New 5.11.6

## Syntax

`WEAPONREACH:x`

## Parameters

-   x: Formula (Weapon Reach)



What it does
------------

Defines the formula used to calculate a weapons reach. Three variables
are used in the formula, RACEREACH, REACH and REACHMULT. RACEREACH is
the value of the [REACH](/list/data/races/reach.html) tag set in the
PC's race. REACH is the value of the
[REACH](/list/data/equipment/reach.html) tag set in the Weapon, if no
REACH tag is present the value defaults to 5. REACHMULT is the value of
the [REACHMULT](/list/data/equipment/reachmult.html) tag set in the
weapon, if no REACHMULT tag is present the value is 1.

Example
-------

`WEAPONREACH:(RACEREACH+(max(0,REACH-5)))*REACHMULT`

This is the standard formula used in the 35e gameMode.

