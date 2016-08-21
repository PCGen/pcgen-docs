+++
date = "2016-08-01"
title = "MULT (Data: abilities.lst)"
original_url = "list/data/ability.html#mult"
categories = [ "all-tag", "ability-tag" ]
+++

## Status

Added 5.11.x

## Syntax

`MULT:x`

## Parameters

-   x: Boolean ('YES' or 'NO')



What it does
------------

-   This determines if an ability can be taken multiple times. If the
    value is set to 'YES', then you **MUST** also use a `CHOOSE` tag.
-   **.MOD Behavior:** When modifying an ability with the `.MOD` tag,
    given an existing `MULT` tag, the data included in a new `MULT` tag
    will overwrite the existing tag data.

Example
-------

`MULT:YES`

This Ability can be taken multiple times.

**Default Value:**

`NO`

**.MOD Example:**

Initial Ability:
`CATEGORY=<category name>|<ability name> <tab> MULT:YES`

Modified By: `CATEGORY=<category name>|<ability name> <tab> MULT:NO`

Is Equivalent To:
`CATEGORY=<category name>|<ability name> <tab> MULT:NO`

Modified ability cannot be taken multiple times.

