+++
date = "2016-08-01"
title = "PRESPELLTYPE (Global: PRErequisite)"
original_url = "/list/global/pre.html#prespelltype"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRESPELLTYPE"
    parent = "global_pre"
+++

## Status

Updated 5.10

## Syntax

`PRESPELLTYPE:x,y=z`

## Parameters

-   x: Number (Number of spells known).
-   y: Arcane (Arcane type spells).
-   y: Divine (Divine type spells).
-   y: Psionic (Psionic type spells).
-   y: ANY (Any type of spell).
-   z: Number (Spell level).



What it does
------------

-   Sets spell type requirements. (Number of spells known of a specific
    type and level.)
-   Use two, or more, PRESPELLTYPE tags if more than one spell type is
    required

Example
-------

`PRESPELLTYPE:4,Arcane=5`

Character must have at least four 5th level arcane spells to meet the
requirement.

`PRESPELLTYPE:1,Arcane=3,Divine=3,Psionic=3`

Character must have at least one 3rd level spell from any of the
"Arcane", "Divine", or "Psionic" types.

`PRESPELLTYPE:1,Arcane=3 <tab> PRESPELLTYPE:1,Divine=3`

Character must have at least one 3rd level "Arcane" type spell and one
3rd level "Divine" type spell.

