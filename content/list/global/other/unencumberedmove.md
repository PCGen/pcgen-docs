+++
date = "2016-08-01"
title = "UNENCUMBEREDMOVE (Global: OTHER)"
original_url = "list/global/other.html#unencumberedmove"
categories = [ "all-tag", "other-tag" ]
+++

## Status

New 5.5.2

## Syntax

`UNENCUMBEREDMOVE:x`

## Parameters

-   x: LightLoad
-   x: MediumLoad
-   x: HeavyLoad
-   x: Overload
-   x: LightArmor
-   x: MediumArmor
-   x: HeavyArmor



What it does
------------

This is a global tag that allows the character to ignore encumbrance
penalties to movement.

This tag is backwards inclusive, so if you have
UNENCUMBEREDMOVE:MediumLoad it means you also have
UNENCUMBEREDMOVE:LightLoad.

This can be | (pipe) delimited in order to negate both the encumbrance
and armor penalties.

Example
-------

`UNENCUMBEREDMOVE:HeavyLoad|HeavyArmor`

This is used in the Race entry for Dwarves, Dwarves ignore encumbrance
penalties to movement for heavy armor and heavy loads.

