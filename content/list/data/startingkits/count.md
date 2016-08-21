+++
date = "2016-08-01"
title = "COUNT (Data: starting_kits.lst)"
original_url = "list/data/startingkits.html#count"
categories = [ "all-tag", "startingkits-tag" ]
+++

## Status

New 5.8

## Syntax

`COUNT:x`

## Parameters

-   x: Number (Maximum number of choices to allow)



What it does
------------

-   Sets the maximum number of choices that can be made from the list.
-   This tag is optional; if not present it defaults to one.
-   This tag will have no effect unless the primary tag contains a list.

Where it is used
----------------

Examples
--------

`FEAT:Dodge|Improved Initiative|Alertness <tab> COUNT:2`

Would allow the choice of two of Dodge, Improved Initiative, and
Alertness.

`PROF:Longsword|Rapier|Longbow|Shortbow <tab> COUNT:2`

Would allow the choice of two of Longsword, Rapier, Longbow, and
Shortbow.

`SPELLS:LEVEL=1 <tab> COUNT:2`

Would allow the choice of two first level spells.

Where it is used
----------------

SKILL, DOMAIN, FEAT, PROF, or SPELLS lines

