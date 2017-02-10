+++
date = "2016-08-01"
title = "STACK (Data: abilities.lst)"
original_url = "/list/data/ability.html#stack"
categories = [ "all-tag", "ability-tag" ]
[menu.main]
    name = "STACK"
    parent = "data_ability"
+++

## Status

None

## Syntax

`STACK:x`

## Parameters

-   x: Boolean ('YES' or 'NO')



<span id="stack"></span> \*\*\* Added 5.11.x

What it does
------------

-   This tells PCGen if the ability benefits may be stacked on
    one another.
-   **.MOD Behavior:** When modifying an ability with the `.MOD` tag,
    given an existing `STACK` tag, the data included in a new `STACK`
    tag will overwrite the existing tag data.

Example
-------

`STACK:YES`

The benefits for this ability stack with itself if taken multiple times.

**Default Value:**

`NO`

**.MOD Example:**

Initial Ability:
`CATEGORY=<category name>|<ability name> <tab> STACK:YES`

Modified By: `CATEGORY=<category name>|<ability name> <tab> STACK:NO`

Is Equivalent To:
`CATEGORY=<category name>|<ability name> <tab> STACK:NO`

The benefits for the modified ability will not stack with itself if
taken multiple times.

