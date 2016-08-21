+++
date = "2016-08-01"
title = "BONUSCHECKS (Game Mode: statsandchecks.lst)"
original_url = "list/system/gamemode-statsandchecks.html#bonuschecks"
categories = [ "all-tag", "gamemode-statsandchecks-tag" ]
+++

## Status

None

## Syntax

`BONUS:CHECKS|x|y`

## Parameters

-   x: Text (The name to be used for display on the
    character sheet - should be all caps).
-   y: Text (The three letter abbreviation of the stat
    that this save is based on - should be all caps).



What it does
------------

Defines what stat gives a bonus to what check (BONUS:CHECKS is the ONLY
statement that will work on CHECKNAME lines, besides the CHECKNAME tag
itself).

Example
-------

`BONUS:CHECKS|FORTITUDE|CON`

Defines that "Constitution" gives a bonus to "Fortitude" checks.

Where it is used
----------------

CHECKNAME Line.

**Complete Line Example:**

`CHECKNAME:Fortitude BONUS:CHECKS|FORTITUDE|CON`

