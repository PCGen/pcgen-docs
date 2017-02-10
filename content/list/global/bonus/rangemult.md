+++
date = "2016-08-01"
title = "RANGEMULT (Global: BONUS)"
original_url = "/list/global/bonus.html#rangemult"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "RANGEMULT"
    parent = "global_bonus"
+++

## Status

None

## Syntax

`BONUS:RANGEMULT|x|y`

## Parameters

-   x: Text (PROJECTILE or THROWN)
-   y: Number, variable or formula (Number to add
    to range)



What it Does
------------

-   Increases range by percent.
-   PROJECTILE and THROWN are hardcoded types (will be changed later).
-   See also RANGEADD and POSTRANGEADD.
-   RANGEMULT will be applied after all RANGEADD tags, but before all
    POSTRANGEADD tags.

Examples
--------

`BONUS:RANGEMULT|PROJECTILE|50`

Would increase the range of projectile weapons by 50% (x1.5).

`BONUS:RANGEMULT|PROJECTILE|-50`

Would decrease the range of projectile weapons by 50% (x.5).

`BONUS:RANGEMULT|THROWN|100`

Would increase the range of thrown weapons by 100% (x2).

`BONUS:RANGEMULT|TYPE=Starship|50`

Would increase the range of starship weapons by 50% (x1.5).

