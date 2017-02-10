+++
date = "2016-08-01"
title = "SPELLBASEDC (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#spellbasedc"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "SPELLBASEDC"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_SPELLBASEDC"
+++

## Status

None

## Syntax

`SPELLBASEDC:x`

## Parameters

-   x: Formula (used to determine a spells base DC)



What it does
------------

This formula is used to determine the starting BASE DC for a spell.

Example
-------

`SPELLBASEDC:10+SPELLLEVEL+BASESPELLSTAT`

Takes the number 10 as the starting point, then it adds the spells level
and finally the primary stat bonus of the caster to come to the total.

