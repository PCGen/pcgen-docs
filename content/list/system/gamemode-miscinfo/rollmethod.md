+++
date = "2016-08-01"
title = "ROLLMETHOD (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#rollmethod"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "ROLLMETHOD"
    parent = "system_gamemode-miscinfo"
+++

## Status

New 5.9.3

## Syntax

`ROLLMETHOD:x`

## Parameters

-   x: Text (Description of random Stat
    rolling method).



What it does
------------

Begins a line which adds a random dice rolling method to generate stats.
This tag is followed by the
[METHOD](/list/system/gamemode-miscinfo/method.html) tag which defines
the actual dice formula. See the entry for
[METHOD](/list/system/gamemode-miscinfo/method.html) for syntax usage.
When a ROLLMETHOD has been added to a miscinfo.lst file it will appear
in it's own menu under the [abilities preference
pane](/menu/settings/character/ability-score.html) as an option to
generate ability stats. If selected this will cause a button labeled
Roll to appear in the Summary window allowing the user to regenerate
ability scores using the method selected.

Example
-------

`ROLLMETHOD:3d6 <tab> METHOD:3d6`

Menu displays "3d6" as the label for this method and simulates rolling 3
six sided dice.

`ROLLMETHOD:4d6 drop lowest <tab> METHOD:roll(4,6,[2,3,4])`

Menu displays "4d6 drop lowest" as the label for this method.

`ROLLMETHOD:5d6 drop 2 lowest <tab> METHOD:roll(5,6,[3,4,5])`

Menu displays "5d6 drop 2 lowest" as the label for this method.

