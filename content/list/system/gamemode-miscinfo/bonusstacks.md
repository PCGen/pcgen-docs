+++
date = "2016-08-01"
title = "BONUSSTACKS (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#bonusstacks"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "BONUSSTACKS (Game Mode: miscinfo.lst)"
    parent = "gamemode-miscinfo"
+++

## Status

New 5.9.5

## Syntax

`BONUSSTACKS:x.x`

## Parameters

-   x: Text (Bonus Type)



What it does
------------

This is a list of all bonuses which stack. Tags which do not have a
TYPE=label parameter are assumed to stack, tags which do have a
TYPE=label parameter do not normally stack. Some games have exceptions
to this rule and list specific types which always do stack. In the
fantasy gameModes Dodge and Circumstance always stack. This tag lists
those exceptions. The Types can be listed all in one tag or multiple
tags can be used.

Example
-------

`BONUSSTACKS:Defense.Dodge.Circumstance.NotRanged.NotFlatFooted`

The listed Types will stack.

`BONUSSTACKS:Defense`

`BONUSSTACKS:Dodge`

`BONUSSTACKS:Circumstance`

`BONUSSTACKS:NotRanged`

`BONUSSTACKS:NotFlatFooted`

The listed Types will stack.

