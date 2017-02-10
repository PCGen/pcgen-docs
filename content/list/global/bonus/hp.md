+++
date = "2016-08-01"
title = "HP (Global: BONUS)"
original_url = "/list/global/bonus.html#hp"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "HP"
    parent = "global_bonus"
    identifier = "global_bonus_HP"
+++

## Status

None

## Syntax

`BONUS:HP|x|y`

## Parameters

-   x: ALTHP
-   x: CURRENTMAX
-   y: Number, variable or formula (Number to add to
    hit points, as defined in miscinfo.lst)



What it Does
------------

-   Adds to the number of either the current maximum ( **CURRENTMAX** )
    hit points or to the secondary ( **ALTHP** ) hit points.
-   Both **CURRENTMAX** and **ALTHP** hit points are defined in the
    <span class="lstfile"> miscinfo.lst </span> file.

Example
-------

`BONUS:HP|ALTHP|3`

Adds three to the total secondary hit points.

`BONUS:HP|ALTHP|5|TYPE=Species`

Adds five to the total secondary hit points for species reasons.

`BONUS:HP|CURRENTMAX|2`

Character gains two additional hit points.

`STACK:NO <tab> MULT:YES <tab> CHOOSE:NUMCHOICES=1|STAT|CON <tab> BONUS:HP|CURRENTMAX|%LIST-CON`

Character gains between 1 and CON Bonus additional hit points, can be
used multiple time, does not stack.

`TEMPBONUS:PC|HP|CURRENTMAX|AidSoulHitPoints*%CHOICE|TYPE=Temporary`

Character gains additional hit points temporary based on the
calculation.

