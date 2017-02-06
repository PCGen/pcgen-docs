+++
date = "2016-08-01"
title = "RANGEADD (Global: BONUS)"
original_url = "/list/global/bonus.html#rangeadd"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "RANGEADD (Global: BONUS)"
    parent = "bonus"
+++

## Status

None

## Syntax

`BONUS:RANGEADD|x|y`

## Parameters

-   x: Text (PROJECTILE or THROWN)
-   y: Number, variable or formula (Number to add
    to range)



What it Does
------------

-   Increases range by integer.
-   PROJECTILE and THROWN are hardcoded types (will be changed later).
-   See also RANGEMULT and POSTRANGEADD.
-   RANGEADD will be applied before any RANGEMULT and POSTRANGEADD tags.

Examples
--------

`BONUS:RANGEADD|PROJECTILE|5`

Would increase the range of projectile weapons by 5.

`BONUS:RANGEADD|THROWN|10`

Would increase the range of thrown weapons by 10.

