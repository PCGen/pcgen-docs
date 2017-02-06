+++
date = "2016-08-01"
title = "SAVE (Global: BONUS)"
original_url = "/list/global/bonus.html#save"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "SAVE (Global: BONUS)"
    parent = "bonus"
+++

## Status

New 6.03.00

## Syntax

`BONUS:SAVE|x,x|y`

## Parameters

-   x: Text (Save name)
-   x: BASE.Text (Save name)
-   x: ALL
-   y: Number, variable or formula (Save Bonus)



What it Does
------------

-   Adds to the indicated save.
-   Using the `BASE.x` syntax adds to indicated base save (normally only
    used in class progressions).
-   Valid saves, e.g. Fortitude,Reflex,Will, are defined in
    the GameMode.
-   Substitution is allowed through the use of `%LIST` .

Example
-------

`BONUS:SAVE|Fortitude,Reflex|1`

Adds one to "Fortitude" and "Reflex" saves.

`CHOOSE:NUMCHOICES=1|CHECKS|Fortitude|Reflex|Will <tab> BONUS:SAVE|%LIST|1`

The selection, "Fortitude", "Reflex" or "Will", is put into the
`BONUS:SAVE` tag in place of the `%LIST`

`BONUS:SAVE|Willpower||max(CHA,WIS)-WIS`

How does one code up something like 'you can add your Charisma modifier
instead of Wisdom for Willpower saves'?

`BONUS:SAVE|Fortitude|2|TYPE=Resistance`

Adds two to Fortitude saves due to Resistance.

`BONUS:SAVE|BASE.Fortitude,BASE.Reflex|1`

Adds one to the base "Fortitude" and "Reflex" saves.

`BONUS:SAVE|ALL|1`

Adds one to the all saves.

`TEMPBONUS:ANYPC|SAVE|ALL|3|TYPE=Morale`

Adds three to all saves, due to morale, to all PC Characters.

