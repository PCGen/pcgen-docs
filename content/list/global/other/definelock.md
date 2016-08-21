+++
date = "2016-08-01"
title = "DEFINELOCK (Global: OTHER)"
original_url = "list/global/other.html#definelock"
categories = [ "all-tag", "other-tag" ]
+++

## Status

deprecated 6.01.03 - Remove for 6.4 - Use DEFINESTAT

## Syntax

`DEFINE:LOCK.x|y`

## Parameters

-   x: Ability Score (STR, DEX, CON, INT, CHA, WIS or
    other stat defined in the gameMode)
-   y: Number (Value stat is to be locked to)



What it does
------------

Locks the specified ability score to a specific value regardless of any
other bonuses to that ability. If the locked value is 10 the OS will
output an asterisk (\*) instead of the number. This is commonly used
when a creature has a non-ability such as the undead's lack of a
constitution score.

Example
-------

`DEFINE:LOCK.CON|10`

Constitution is set to 10 and an asterisk is output.

Example Conversion to DEFINESTAT tag
------------------------------------

`DEFINE:LOCK.CON|10` becomes `DEFINESTAT:LOCK|CON|10`

