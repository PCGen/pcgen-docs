+++
date = "2016-08-01"
title = "MISC (Global: BONUS)"
original_url = "/list/global/bonus.html#misc"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "MISC"
    parent = "global_bonus"
    identifier = "global_bonus_MISC"
+++

## Status

Updated 5.13.6

## Syntax

`BONUS:MISC|x|y`

## Parameters

-   x: ACCHECK
-   x: CR
-   x: MAXDEX
-   x: SPELLFAILURE
-   x: SR
-   y: Number, variable or formula (Number to apply as
    a bonus)



What it Does
------------

Modifies the parameter specified:

-   **ACCHECK** - Armor Check Penalty
-   **CR** - Challenge Rating
-   **MAXDEX** - Maximum Dexterity Bonus
-   **SPELLFAILURE** - Arcane Spell Failure
-   **SR** - Spell Resistance

Example
-------

`BONUS:MISC|ACCHECK|1`

Adds one to total Armor Check.

`BONUS:MISC|CR|2`

Adds 2 to the challange rating.

`BONUS:MISC|MAXDEX|1`

Adds one to total Maximum Dex allowed while wearing armor.

`BONUS:MISC|SPELLFAILURE|20|PREEQUIP:2,TYPE=Armor,TYPE=Light`

Adds 20% to Spell Failure chance if equipped with light armor.

`BONUS:MISC|SR|10+CL|TYPE=EbonLink`

Adds 10 plus the Character Level to the spell resistance due to
EbonLink.

