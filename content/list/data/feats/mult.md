+++
date = "2016-08-01"
title = "MULT (Data: feats.lst)"
original_url = "/list/data/feats.html#mult"
categories = [ "all-tag", "feats-tag" ]
[menu.main]
    name = "MULT (Data: feats.lst)"
    parent = "feats"
+++

## Status

None

## Syntax

`MULT:x`

## Parameters

-   x: Boolean (YES/NO)



What it does
------------

-   This determines if a feat can be taken multiple times. If the value
    is set to YES, then you **MUST** also use a `CHOOSE` tag.
-   **.MOD Behavior:** When modifying an feat with the `.MOD` tag, given
    an existing `MULT` tag, the data included in a new `MULT` tag will
    overwrite the existing tag data.

Example
-------

`MULT:YES`

This Feat can be taken multiple times.

**Default Value:**

`NO`

**.MOD Example:**

Initial Feat: `<feat name> <tab> MULT:YES`

Modified By: `<feat name> <tab> MULT:NO`

Is Equivalent To: `<feat name> <tab> MULT:NO`

Modified feat cannot be taken multiple times.

