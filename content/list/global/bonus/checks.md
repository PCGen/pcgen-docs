+++
date = "2016-08-01"
title = "CHECKS (Global: BONUS)"
original_url = "list/global/bonus.html#checks"
categories = [ "all-tag", "bonus-tag" ]
+++

## Status

deprecated 6.03.00 - Remove for 6.6 - Use BONUS:SAVE

## Syntax

`BONUS:CHECKS|x,x|y`

## Parameters

-   x: Text (Check name)
-   x: BASE.Text (Check name)
-   x: ALL
-   y: Number, variable or formula (Save Bonus)



What it Does
------------

-   Adds to the indicated check.
-   Using the `BASE.x` syntax adds to indicated base check (normally
    only used in class progressions).
-   Valid checks, e.g. Fortitude,Reflex,Will, are defined in
    the GameMode.
-   Substitution is allowed through the use of `%LIST` .

Example
-------

`BONUS:CHECKS|Fortitude,Reflex|1`

Adds one to "Fortitude" and "Reflex" saves.

`CHOOSE:NUMCHOICES=1|CHECK|Fortitude|Reflex|Will <tab> BONUS:CHECKS|%LIST|1`

The selection, "Fortitude", "Reflex" or "Will", is put into the
`BONUS:CHECKS` tag in place of the `%LIST`

`BONUS:CHECKS|Willpower||max(CHA,WIS)-WIS`

How does one code up something like 'you can add your Charisma modifier
instead of Wisdom for Willpower saves'?

`BONUS:CHECKS|Fortitude|2|TYPE=Resistance`

Adds two to Fortitude checks due to Resistance.

`BONUS:CHECKS|BASE.Fortitude,BASE.Reflex|1`

Adds one to the base "Fortitude" and "Reflex" saves.

`BONUS:CHECKS|ALL|1`

Adds one to the all saves.

`TEMPBONUS:ANYPC|CHECKS|ALL|3|TYPE=Morale`

Adds three to all saves, due to morale, to all PC Characters.

