+++
date = "2016-08-01"
title = "DEFINEUNLOCK (Global: OTHER)"
original_url = "/list/global/other.html#defineunlock"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "DEFINEUNLOCK"
    parent = "global_other"
+++

## Status

deprecated 6.01.03 - Remove for 6.4 - Use DEFINESTAT

## Syntax

`DEFINE:UNLOCK.x`

## Parameters

-   x: Ability Score (STR, DEX, CON, INT, CHA, WIS or
    other stat defined in the gameMode)



What it does
------------

Unlocks a stat which has been locked by DEFINE:LOCK

This tag will always override DEFINE:LOCK

Example
-------

`DEFINE:UNLOCK.CON`

Constitution is unlocked.

Example Conversion to DEFINESTAT tag
------------------------------------

`DEFINE:UNLOCK.CON` becomes `DEFINESTAT:UNLOCK|CON`

