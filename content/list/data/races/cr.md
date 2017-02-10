+++
date = "2016-08-01"
title = "CR (Data: races.lst)"
original_url = "/list/data/races.html#cr"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "CR"
    parent = "data_races"
+++

## Status

None

## Syntax

`CR:x`

## Parameters

-   x: Number (Challenge rating)



What it does
------------

-   Sets the Challenge Rating of the creature. For CR's less than 1,
    fractions are used (1/2, 1/4, 1/8).
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `CR` tag, the data included in a new `CR` tag will
    overwrite the existing tag data.

**Note:** CR's using fractions must start with a "1/". Expressions such
as CR:3/4 or CR:0.5 will not work.

Example
-------

`CR:1/4`

Race is rated at a quarter challenge rating.

**.MOD Example:**

Initial Race: `Boar <tab> CR:2`

Modified By: `Boar.MOD <tab> CR:3`

Results In: `Boar <tab> CR:3`

The Boar's CR is set to 3.

