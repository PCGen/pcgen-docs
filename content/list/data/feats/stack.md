+++
date = "2016-08-01"
title = "STACK (Data: feats.lst)"
original_url = "/list/data/feats.html#stack"
categories = [ "all-tag", "feats-tag" ]
[menu.main]
    name = "STACK"
    parent = "data_feats"
    identifier = "data_feats_STACK"
+++

## Status

None

## Syntax

`STACK:x`

## Parameters

-   x: Boolean (YES/NO)



What it does
------------

-   This tells PCGen if the feat benefits may be stacked on one another.
-   **.MOD Behavior:** When modifying a feat with the `.MOD` tag, given
    an existing `STACK` tag, the data included in a new `STACK` tag will
    overwrite the existing tag data.

Example
-------

`STACK:YES`

This Feat may be stack on itself.

**Default Value:**

`NO`

**feat.MOD Example:**

Initial Feat: `<feat name> <tab> STACK:YES`

Modified By: `<feat name> <tab> STACK:NO`

Is Equivalent To: `<feat name> <tab> STACK:NO`

The benefits for the modified feat will not stack with itself if taken
multiple times.

