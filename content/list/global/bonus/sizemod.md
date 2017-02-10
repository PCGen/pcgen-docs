+++
date = "2016-08-01"
title = "SIZEMOD (Global: BONUS)"
original_url = "/list/global/bonus.html#sizemod"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "SIZEMOD"
    parent = "global_bonus"
+++

## Status

None

## Syntax

`BONUS:SIZEMOD|NUMBER|x`

## Parameters

-   x: Number, variable or formula (Number of size
    categories to adjust)



What it Does
------------

-   Moves the character's size up or down the size range by the
    indicated number of steps.
-   All stat modifications caused by a size change will take effect.
-   Size Categories in order are: Fine, Diminutive, Tiny, Small, Medium,
    Large, Huge, Gargantuan, Colossal.

Examples
--------

`BONUS:SIZEMOD|NUMBER|1`

Adds one to size. A "Medium" character would become "Large".

`BONUS:SIZEMOD|NUMBER|-2`

Reduces size by two. A "Medium" character would become "Tiny".

`BONUS:SIZEMOD|NUMBER|1|PRESIZEGT:T`

If size is greater than Tiny (T) add 1 to SIZEMOD.

`BONUS:SIZEMOD|NUMBER|-1|PRERACE:Wolf,Dire Animal (Dire Rat)|PREVARGT:TL,3|PREVARLT:TL,7`

If Total Levels (TL) are more than 3 and less than 7, and you are a Dire
Wolf, reduce the SIZEMOD by 1.

`BONUS:SIZEMOD|NUMBER|-1|PRERACE:Wolf,Dire Animal (Dire Rat)|PREVARGT:TL,3|PREVARLT:TL,7.CLEAR`

Removes the if Total Levels (TL) are more than 3 and less than 7, and
you are a Dire Wolf, reduce the SIZEMOD by 1.

`BONUS:SIZEMOD|NUMBER|1|PRESIZEGT:T.MOD <tab> BONUS:SIZEMOD|NUMBER|2|PRESIZEGT:T`

Changes the if size is greater than Tiny (T) add 1 to SIZEMOD to add 2
to the SIZEMOD.

`TEMPBONUS:PC|SIZEMOD|NUMBER|1`

Add 1 to SIZEMOD of any PC.

