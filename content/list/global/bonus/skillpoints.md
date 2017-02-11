+++
date = "2016-08-01"
title = "SKILLPOINTS (Global: BONUS)"
original_url = "/list/global/bonus.html#skillpoints"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "SKILLPOINTS"
    parent = "global_bonus"
    identifier = "global_bonus_SKILLPOINTS"
+++

## Status

None

## Syntax

`BONUS:SKILLPOINTS|NUMBER|x`

## Parameters

-   x: Number, variable or formula (Number to add to
    skill level)



What it Does
------------

-   Adds to the number of skill ranks gained when the character gains
    a level.
-   Not retroactive.
-   PRExxx tags may be used with this tag. Exception: Do NOT mix
    PRELEVELMAX with this tag.

Examples
--------

`BONUS:SKILLPOINTS|NUMBER|1`

Adds one skill point per level.

`BONUS:SKILLPOINTS|NUMBER|4|PRELEVELMAX:1`

Adds 4 additional skillpoints to the character at first level only,
above and beyond any other skillpoints gained for race or class, etc.

`BONUS:SKILLPOINTS|NUMBER|6|PRELEVELMAX:3`

Adds 6 additional skillpoints to the character at first to third levels
only, above and beyond any other skillpoints gained for race or class,
etc.

