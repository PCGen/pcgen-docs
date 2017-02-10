+++
date = "2016-08-01"
title = "SAB (Global: ADD)"
original_url = "/list/global/add.html#sab"
categories = [ "all-tag", "add-tag" ]
[menu.main]
    name = "SAB"
    parent = "global_add"
    identifier = "global_add_SAB"
+++

## Status

New 5.13.7

## Syntax

`ADD:SAB|x|y|z,z`

## Parameters

-   x: Text (Name displayed on the chooser dialog.)
-   y: Number, Variable or Formula (Optional - Number
    of choices granted)
-   z: Text (Special ability name or description.)



What it does
------------

-   Will add a number (y) of special abilities, from the presented list
    of special abilities (y), to the character.
-   If the count (y) is not used the first special ability will
    be selected.
-   If count (y) is used the character will be given a choice of one to
    the limit of count (y) from the items listed (z).
-   Special Abilities listed are a comma-delimited (,) list.

Example
-------

`ADD:SAB|Brick Wall|3|Damage Reduction,Concussion Resistance,Remain Concious, Melee Smash,Extreme Effort`

Add three of special abilities listed.

`ADD:SAB|Shadow Slayer|1|Detect Shadow,Shadow Immunity`

Add one of the two special abilities.

