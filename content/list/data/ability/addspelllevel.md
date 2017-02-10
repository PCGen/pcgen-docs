+++
date = "2016-08-01"
title = "ADDSPELLLEVEL (Data: abilities.lst)"
original_url = "/list/data/ability.html#addspelllevel"
categories = [ "all-tag", "ability-tag" ]
[menu.main]
    name = "ADDSPELLLEVEL"
    parent = "data_ability"
    identifier = "data_ability_ADDSPELLLEVEL"
+++

## Status

None

## Syntax

`ADDSPELLLEVEL:x`

## Parameters

-   x: Number (Increase in spell slot level)



<span id="addspelllevel"></span> \*\*\* Added 5.11.x

What it does
------------

-   This tag is used in metamagic abilities to denote how much higher
    the spell levelslot requires.
-   **.MOD Behavior:** When modifying an ability with the `.MOD` tag,
    given an existing `ADDSPELLLEVEL` tag, the data included in a new
    `ADDSPELLLEVEL` tag will overwrite the existing tag data.

Example
-------

`ADDSPELLLEVEL:2`

A spell with this metamagic ability applied to it takes up a slot two
levels higher than the normal spell.

**.MOD Example:**

Initial Ability:
`CATEGORY=<category name>|<ability name> <tab> ADDSPELLLEVEL:1`

Modified By:
`CATEGORY=<category name>|<ability name> <tab> ADDSPELLLEVEL:2`

Is Equivalent To:
`CATEGORY=<category name>|<ability name> <tab> ADDSPELLLEVEL:2`

Modified ability applied to a spell will cause the spell to take up a
slot two levels higher than the normal spell.

