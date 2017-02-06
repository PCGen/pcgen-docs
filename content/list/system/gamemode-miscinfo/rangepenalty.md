+++
date = "2016-08-01"
title = "RANGEPENALTY (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#rangepenalty"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "RANGEPENALTY (Game Mode: miscinfo.lst)"
    parent = "gamemode-miscinfo"
+++

## Status

None

## Syntax

`RANGPENALTY:x`

## Parameters

-   x: Number



What it does
------------

-   Sets the standard modification of the to-hit value for each range
    increment after the first.
-   Penalty defaults to zero if this tag is not present.

Example
-------

`RANGEPENALTY:-2`

Sets the range penalty for those range increments beyond the first to
-2.

