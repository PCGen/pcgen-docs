+++
date = "2016-08-01"
title = "CRMOD (Data: races.lst)"
original_url = "list/data/races.html#crmod"
categories = [ "all-tag", "races-tag" ]
+++

## Status

New 6.1.2

## Syntax

`CRMOD:x.x|y`

## Parameters

-   x: Text (a class type as defined in the game mode).
-   y: Formula (a standard PCGen LST formula).



What it does
------------

Overrule the CRMODs from the game mode for creatures of the race. The
CRMOD is set to the value of y for all class types specified as x

Example
-------

`CRMOD:PC.NPC|0`

In the Pathfinder RPG, a drow noble's CR is always equal to his
character level.

`CRMOD:NPC|-3`

In the Pathfinder RPG, the CR of a kobold with only NPC classes is equal
to his character level minus 3.

