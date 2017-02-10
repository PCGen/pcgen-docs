+++
date = "2016-08-01"
title = "STATRANGE2 (Game Mode: statsandchecks.lst)"
original_url = "/list/system/gamemode-statsandchecks.html#statrange2"
categories = [ "all-tag", "gamemode-statsandchecks-tag" ]
[menu.main]
    name = "STATRANGE2"
    parent = "system_gamemode-statsandchecks"
    identifier = "system_gamemode-statsandchecks_STATRANGE2"
+++

## Status

None

## Syntax

`STATRANGE:x`

## Parameters

-   x: Number (The increment in the score necessary to
    get another bonus spell slot of the indicated level).



What it does
------------

Indicates the increment in the spellcasting ability score necessary for
the bonus spell granted on this line to be given again.

Example
-------

`STATRANGE:8`

Base stat score +8 is required before another spell is given.

Where it is used
----------------

BONUSSPELLLEVEL Line.

**Complete Line Example:**

`BONUSSPELLLEVEL:1 BASESTATSCORE:12 STATRANGE:8`

