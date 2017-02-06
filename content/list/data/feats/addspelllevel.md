+++
date = "2016-08-01"
title = "ADDSPELLLEVEL (Data: feats.lst)"
original_url = "/list/data/feats.html#addspelllevel"
categories = [ "all-tag", "feats-tag" ]
[menu.main]
    name = "ADDSPELLLEVEL (Data: feats.lst)"
    parent = "feats"
+++

## Status

Updated 5.16.0

## Syntax

`ADDSPELLLEVEL:x`

## Parameters

-   x: Number (Increase in spell slot level)



What it does
------------

-   This tag is used in metamagic feats to denote how much higher the
    spell level slot requires.
-   **.MOD Behavior:** When modifying a a feat with the `.MOD` tag,
    given an existing `ADDSPELLLEVEL` tag, the data included in a new
    `ADDSPELLLEVEL` tag will overwrite the existing tag data.

Example
-------

`ADDSPELLLEVEL:2`

A spell with this metamagic feat applied to it takes up a slot two
levels higher than the normal spell.

**.MOD Example:**

Initial Feat: `<feat name> <tab> ADDSPELLLEVEL:1`

Modified By: `<feat name> <tab> ADDSPELLLEVEL:2`

Is Equivalent To: `<feat name> <tab> ADDSPELLLEVEL:2`

Modified feat applied to a spell will causes the spell to take up a slot
two levels higher than the normal spell.

