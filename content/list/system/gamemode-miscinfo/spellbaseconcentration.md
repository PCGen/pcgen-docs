+++
date = "2016-08-01"
title = "SPELLBASECONCENTRATION (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#spellbaseconcentration"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "SPELLBASECONCENTRATION"
    parent = "system_gamemode-miscinfo"
    identifier = "system_gamemode-miscinfo_SPELLBASECONCENTRATION"
+++

## Status

New 5.17.7

## Syntax

`SPELLBASECONCENTRATION:x`

## Parameters

-   x: Formula (used to determine a spells base
    concentration check bonus)



What it does
------------

This formula is used to determine the starting **BASE** concentration
check bonus for a spell.

**NOTE:** If the game mode does not contain a
[SPELLBASECONCENTRATION](/list/system/gamemode-miscinfo/spellbaseconcentration.html)
tag, the output tokens
[SPELLLISTCLASS.y.CONCENTRATION](/outputsheet/tokens/spell.html#spelllist)
and
[SPELLMEM.v.w.x.y.CONCENTRATION](/outputsheet/tokens/spell.html#spellmem)
will generate an empty string. Output sheets should check the value of
these tokens, and if empty should not display concentration check
bonuses.

Example
-------

`SPELLBASECONCENTRATION:CASTERLEVEL+BASESPELLSTAT`

Adds the spell's caster level and the primary stat bonus of the caster
to come to the total.

