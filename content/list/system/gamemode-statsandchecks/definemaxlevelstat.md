+++
date = "2016-08-01"
title = "DEFINEMAXLEVELSTAT (Game Mode: statsandchecks.lst)"
original_url = "list/system/gamemode-statsandchecks.html#definemaxlevelstat"
categories = [ "all-tag", "gamemode-statsandchecks-tag" ]
+++

## Status

None

## Syntax

`DEFINE:MAXLEVELSTAT:x|y`

## Parameters

-   x: Text (stat abbreviation).
-   y: formula (formula that gives the
    desired maximum).



What it does
------------

Determines the maximum level of spell/ability you can use based on the
referenced stat.

The only known hardcode VAR with a = in it.

Example
-------

`DEFINE:MAXLEVELSTAT:WIS|WISSCORE-10`

Maximum spell level is Wisdom -10 (&lt;ABB&gt;SCORE is the variable name
for the stat value).

Where it is used
----------------

STATNAME Line.

