+++
date = "2016-08-01"
title = "HPFORMULA (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#hpformula"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "HPFORMULA (Game Mode: miscinfo.lst)"
    parent = "gamemode-miscinfo"
+++

## Status

New 5.8.0

## Syntax

`HPFORMULA:x`

## Parameters

-   x: Formula (How to calculate total HP for
    a character).



What it does
------------

-   The HPFORMULA tag is used to set the formula to use to calculate
    total HP for a character.
-   The formula can use any valid JEP expressions.
-   The formula can reference any variables defined for the character.

Examples
--------

`HPFORMULA:SKILLTOTAL=Endurance`

Sets the HP total for a character equal to its skill bonus in the
Endurance skill.

