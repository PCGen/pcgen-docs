+++
date = "2016-08-01"
title = "STATBASESPELLKNOWNSTATCLASS (Global: BONUS)"
original_url = "/list/global/bonus.html#statbasespellknownstatclass"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "STATBASESPELLKNOWNSTATCLASS"
    parent = "global_bonus"
    identifier = "global_bonus_STATBASESPELLKNOWNSTATCLASS"
+++

## Status

New 5.5

## Syntax

`BONUS:STAT|BASESPELLKNOWNSTAT;Class=x|y`

## Parameters

-   x: Text (Class name)
-   y: Number, variable or formula (Number to adjust
    stat bonus by)



What it Does
------------

Adds a virtual bonus to character's base spell stat bonus when PCGen
calculates the number of spells the character knows for the class
specified.

Example
-------

`BONUS:STAT|BASESPELLKNOWNSTAT;Class=Wizard|2`

Adds 2 to character's base spell stat bonus for the Wizard class when
calculating the number of spells known.

