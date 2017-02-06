+++
date = "2016-08-01"
title = "UP (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#up"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "UP (Game Mode: miscinfo.lst)"
    parent = "gamemode-miscinfo"
+++

## Status

None

## Syntax

`UP:x,x`

## Parameters




**Varibles used:** (x) alpha numerical

What it does
------------

This comma (,) delimited value determines the next die value in an
incremental set

Example
-------

`UP:1d8,2d6,3d6,4d6,6d6,8d6,12d6`

Determines the next die in the progression will be 1d8, then 2d6 if
chosen again, etc.

Where it is used
----------------

[BASEDICE](/list/system/gamemode-miscinfo/basedice.html) Line

