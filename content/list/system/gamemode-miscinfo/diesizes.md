+++
date = "2016-08-01"
title = "DIESIZES (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#diesizes"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "DIESIZES"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_DIESIZES"
+++

## Status

New 5.13.6

## Syntax

`DIESIZES:x,x`

## Parameters

-   x: Number (Die size)
-   x: MIN=Number (Minimum die size)
-   x: MAX=Number (Maximum die size)



What it does
------------

-   Used to define the scale used by the `HITDIE` tag to bump a
    character's hit die up or down.
-   The `HITDIE` tag is used in the
    [Class](/list/data/classes/hitdie.html) ,
    [Race](/list/data/races/hitdie.html) and
    [Template](/list/data/templates/hitdie.html) files.
-   `MIN=x` sets the lowest hit die size the "%downNumber" `HITDIE`
    function allow.
-   `MAX=x` sets the highest hit die size the "%upNumber" `HITDIE`
    function will allow.
-   The "%Hup" and "%Hdown" `HITDIE` functions will ignore `MIN` and
    `MAX` and move the hit die the full range of die sizes specified by
    the `DIESIZES` tag.

Example
-------

`DIESIZES:1,2,3,MIN=4,6,8,10,MAX=12,20,100,1000`

Sets the range of hit die sizes used in the gameMode and limits the
`HITDIE` tags "%down" and "%up" functions to "4" and "12" respectively.

