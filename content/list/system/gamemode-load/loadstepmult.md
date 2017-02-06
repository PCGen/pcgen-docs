+++
date = "2016-08-01"
title = "LOADSTEPMULT (Game Mode: load.lst"
original_url = "/list/system/gamemode-load.html#loadstepmult"
categories = [ "all-tag", "gamemode-load-tag" ]
[menu.main]
    name = "LOADSTEPMULT (Game Mode: load.lst"
    parent = "gamemode-load"
+++

## Status

None

## Syntax

`LOADSTEPMULT:x`

## Parameters

-   x: Number (Default number is 10)



<span id="loadstepmult"></span> \*\*\* New 5.11.11

What it does
------------

Used for determining encumbrance limits for values outside the range
defined by the `LOAD` tags

Example
-------

`LOADSTEPMULT:4`\

When the encumbrance limits are exceeded in the SIZEMULT:x|y the y value
switched to 4.

