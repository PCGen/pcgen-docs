+++
date = "2016-08-01"
title = "COST (Data: feats.lst)"
original_url = "list/data/feats.html#cost"
categories = [ "all-tag", "feats-tag" ]
+++

## Status

None

## Syntax

`COST:x`

## Parameters

-   x: Number (feat point cost)



What it does
------------

-   This is how many feat points the feat costs. A decimal value, as the
    example below, would mean that it only costs 1/2 a feat point.
-   **.MOD Behavior:** When modifying a feat with the `.MOD` tag, given
    an existing `COST` tag, the data included in a new `COST` tag will
    overwrite the existing tag data.

Example
-------

`COST:1`

Feat costs one feat point.

`COST:.5`

Feat costs half a feat point.

**Default Value:**

`1`

**.MOD Example:**

Initial Feat: `<feat name> <tab> COST:2`

Modified By: `<feat name> <tab> COST:1`

Is Equivalent To: `<ability name> <tab> COST:1`

Modified Feat costs one feat point.

