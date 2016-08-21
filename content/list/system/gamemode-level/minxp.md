+++
date = "2016-08-01"
title = "MINXP (Game Mode: level.lst)"
original_url = "list/system/gamemode-level.html#minxp"
categories = [ "all-tag", "gamemode-level-tag" ]
+++

## Status

None

## Syntax

`MINXP:x`

## Parameters

-   x: Number or Formula (Experience Points)



What it does
------------

-   Sets the minimum experience points needed to achieve a level.
-   When used in conjunction with the `LEVEL:LEVEL` tag, `MINXP`

Examples
--------

`MINXP:(LEVEL*LEVEL-LEVEL)*500`

The standard formula for level progression for the R/SRD.

