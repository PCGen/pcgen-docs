+++
date = "2016-08-01"
title = "PREKIT (Global: PRErequisite)"
original_url = "/list/global/pre.html#prekit"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREKIT (Global: PRErequisite)"
    parent = "pre"
+++

## Status

New 6.1.9

## Syntax

`PREKIT:x,y,y`

## Parameters

-   x: Number (Number of Kits Required)
-   y: Text (Kit Name)



What it does
------------

-   Checks to see if the character has the specified kit(s).
-   The Kit name is taken from the `STARTPACK` tag for the target kit.
-   This will only work with permenant kits.
-   The percent sign (%) can be used as a trailing wildcard.

Examples
--------

`PREKIT:1,Starting Gold`

Makes sure the character has the 'Starting Gold' kit.

`PREKIT:2,Flumph Abilities,Flumph Skills`

Makes sure the character has both kits

`PREKIT:1,Alchemist's Kit`

Makes sure the character does not have the Alchemist's Kit

`PREKIT:1,Dragon Age%`

Will match both 'Dragon Age 01 \~ Wyrmling' and 'Dragon Age 12 \~ Great
Wyrm''

