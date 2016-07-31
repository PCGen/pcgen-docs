+++
date = "2016-08-01"
title = "MOVE (Global: OTHER)"
original_url = "list/global/other.html#move"
categories = [ "all-tag", "other-tag" ]
+++

## Status

None

## Syntax

`MOVE:x,y,x,y`

## Parameters

-   x: Text (Movement Mode)
-   y: Number (Rate per round)



What it does
------------

Determines the Type and Speed of the different movement types the race
has.

Note: Each race should always have a `MOVE` entry as this is required
for other objects to later adjust the movement.

Example
-------

`MOVE:Walk,30,Fly,10`

This would grant a walking speed of 30 ft per round and a flying speed
of 10 feet per round

**Where it can be used:**

`This can be used anywhere except Equipment and Equipment Mod files.`

