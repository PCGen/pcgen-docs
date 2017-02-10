+++
date = "2016-08-01"
title = "BASESTATSCORE (Game Mode: statsandchecks.lst)"
original_url = "/list/system/gamemode-statsandchecks.html#basestatscore"
categories = [ "all-tag", "gamemode-statsandchecks-tag" ]
[menu.main]
    name = "BASESTATSCORE"
    parent = "system_gamemode-statsandchecks"
+++

## Status

None

## Syntax

`BASESTATSCORE:x`

## Parameters

-   x: Number (The necessary minimum spellcasting
    ability score to receive the bonus).



What it does
------------

Set's the minimum spellcasting ability score necessary to receive this
bonus spell slot. (Spellcasting ability score is WIS for Sorcerers, INT
for Wizards, etc.).

Example
-------

`BASESTATSCORE:12`

Defines that a base stat of 12 is required for bonus spells.

Where it is used
----------------

BONUSSPELLLEVEL Line.

