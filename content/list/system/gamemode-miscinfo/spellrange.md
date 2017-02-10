+++
date = "2016-08-01"
title = "SPELLRANGE (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#spellrange"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "SPELLRANGE"
    parent = "system_gamemode-miscinfo"
+++

## Status

None

## Syntax

`SPELLRANGE:x|y`

## Parameters

-   x: Text (Range name)
-   y: Formula



What it does
------------

Takes the defined name and uses the formula to replace the name in the
Spells.lst under the range.

Each value is a seperate TAG

Example
-------

`SPELLRANGE:CLOSE|floor(CASTERLEVEL/2)*5+25`

Range value would be the caster's level divided by 2 with then times by
5 and add 25 to come to the final value entered

Example: Caster level 2 would return a value of 30

`SPELLRANGE:MEDIUM|(CASTERLEVEL*10)+100`

Formula would determine medium to be the caster's level times 10 + 100

`SPELLRANGE:LONG|(CASTERLEVEL*40)+400`

Formula returns a long value based upon the caster level times 40 plus
400\


