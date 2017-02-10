+++
date = "2016-08-01"
title = "BASEDICE (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#basedice"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "BASEDICE"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_BASEDICE"
+++

## Status

None

## Syntax

`BASEDICE:x`

## Parameters

-   Variables Used: (x) die format



**Uses the following sub tags:** UP DOWN

What it does
------------

Determines the next higher or lower value die in a progression set\
 **NOTE:** This uses the UP and DOWN tags with comma (,) separators and
tabs to separate the tags themselves.

Example
-------

`BASEDICE:1d6 UP:1d8,2d6,3d6,4d6,6d6,8d6,12d6 DOWN:1d4,1d3,1d2,1`

This states the base die is a d6 and determines that the next lowest die
would be a d4, then a d3 and the next highest would be a d8, then 2d.

