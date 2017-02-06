+++
date = "2016-08-01"
title = "COST (Data: abilities.lst)"
original_url = "/list/data/ability.html#cost"
categories = [ "all-tag", "ability-tag" ]
[menu.main]
    name = "COST (Data: abilities.lst)"
    parent = "ability"
+++

## Status

None

## Syntax

`COST:x`

## Parameters

-   x: Number (ability point cost)



<span id="cost"></span> \*\*\* Added 5.11.x

What it does
------------

-   This is how many ability points the ability costs. A decimal value,
    as the example below, would mean that it only costs 1/2 an
    ability point.
-   **.MOD Behavior:** When modifying an ability with the `.MOD` tag,
    given an existing `COST` tag, the data included in a new `COST` tag
    will overwrite the existing tag data.

Example
-------

`COST:1`

Ability costs one ability point.

`COST:.5`

Ability costs half a ability point.

**Default Value:**

`1`

**.MOD Example:**

Initial Ability: `CATEGORY=<category name>|<ability name> <tab> COST:2`

Modified By: `CATEGORY=<category name>|<ability name> <tab> COST:1`

Is Equivalent To: `CATEGORY=<category name>|<ability name> <tab> COST:1`

Ability costs one ability point.

