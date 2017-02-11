+++
date = "2016-08-01"
title = "SKILLCOST_CLASS (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#skillcost_class"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "SKILLCOST_CLASS"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_SKILLCOST_CLASS"
+++

## Status

New 5.8.0

## Syntax

`SKILLCOST_CLASS:x`

## Parameters

-   x: Number (The cost of one skill rank for a
    class skill)



What it does
------------

Specifies the cost of one rank of a class skill.

It cannot be chained with a PRExxx Token.

Example
-------

`SKILLCOST_CLASS:1`

Sets the cost of one rank of a class skill to one skill point.

`SKILLCOST_CROSSCLASS:1|PREFEAT:1,Fast Learner`

Does not work due to the chaining of the PREFEAT.

