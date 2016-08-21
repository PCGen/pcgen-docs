+++
date = "2016-08-01"
title = "POSTRANGEADD (Global: BONUS)"
original_url = "list/global/bonus.html#postrangeadd"
categories = [ "all-tag", "bonus-tag" ]
+++

## Status

None

## Syntax

`BONUS:POSTRANGEADD|x|y`

## Parameters

-   x: Text (PROJECTILE or THROWN)
-   y: Number, variable or formula (Number to add
    to range)



What it Does
------------

-   Increases range by integer.
-   PROJECTILE and THROWN are hardcoded types (will be changed later).
-   See also RANGEMULT and POSTRANGEADD.
-   POSTRANGEADD is applied after all RANGEADD and RANGEMULT tags.

Examples
--------

`BONUS:POSTRANGEADD|PROJECTILE|5`

Would increase the range of projectile weapons by 5.

`BONUS:POSTRANGEADD|THROWN|10`

Would increase the range of thrown weapons by 10.

