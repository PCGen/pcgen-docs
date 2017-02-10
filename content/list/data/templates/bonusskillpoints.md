+++
date = "2016-08-01"
title = "BONUSSKILLPOINTS (Data: templates.lst)"
original_url = "/list/data/templates.html#bonusskillpoints"
categories = [ "all-tag", "templates-tag" ]
[menu.main]
    name = "BONUSSKILLPOINTS"
    parent = "data_templates"
+++

## Status

None

## Syntax

`BONUSSKILLPOINTS:x`

## Parameters

-   x: Number (Number of bonus skill points &gt;0)



What it does
------------

-   The numeric value provided will be multiplied by 4 at first level
    and granted to the character as the beginning skill points while
    subsequent levels will be granted only the numeric value as
    additional skill points.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `BONUSSKILLPOINTS` tag, the data included in a new
    `BONUSSKILLPOINTS` tag will overwrite the existing tag data.

Example
-------

`BONUSSKILLPOINTS:2`

Two bonus skill points are given.

**.MOD Example:**

Initial Template: `Sentient Construct <tab> BONUSSKILLPOINTS:2`

Modified By: `Sentience Construct.MOD <tab> BONUSSKILLPOINTS:3`

Results In: `Sentient Construct <tab> BONUSSKILLPOINTS:3`

Twelve skill points are granted at first level with three being granted
at all subsequent levels.

