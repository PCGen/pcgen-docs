+++
date = "2016-08-01"
title = "BABATTCYC (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#babattcyc"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "BABATTCYC"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_BABATTCYC"
+++

## Status

New 5.4

## Syntax

`BABATTCYC:x`

## Parameters

-   x: Number (difference between a primary attack and
    the subsequent attack).



What it does
------------

Specifies the difference between a primary attack and the subsequent
attack. e.g. for each attack after the first, subtract x to determine
its bonus to hit.

Example
-------

`BABATTCYC:5`

Sets 5 as the difference between each attack in a cycle.

