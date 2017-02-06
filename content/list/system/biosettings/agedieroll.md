+++
date = "2016-08-01"
title = "AGEDIEROLL (System: bio/biosettings.lst)"
original_url = "/list/system/biosettings.html#agedieroll"
categories = [ "all-tag", "biosettings-tag" ]
[menu.main]
    name = "AGEDIEROLL (System: bio/biosettings.lst)"
    parent = "biosettings"
+++

## Status

None

## Syntax

`AGEDIEROLL:x`

## Parameters

-   x: Random Number Formula (Die expression).



What it does
------------

-   Used to randomize the starting age of the character within the
    boundaries of the age set.
-   The closest die roll configuration that would total the difference
    between BASEAGE and MAXAGE at full value.

Examples
--------

`AGEDIEROLL:5d4`

This give a minimum age of 5 and maximum of 20.

`AGEDIEROLL:4d20+1d4`

This give a minimum age of 5 and maximum of 84.

