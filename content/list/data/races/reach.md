+++
date = "2016-08-01"
title = "REACH (Data: races.lst)"
original_url = "/list/data/races.html#reach"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "REACH (Data: races.lst)"
    parent = "races"
+++

## Status

None

## Syntax

`REACH:x`

## Parameters

-   x: Number (Reach in Feet)



What it does
------------

-   Determines the reach of the Race.
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `REACH` tag, the data included in a new `REACH` tag will
    overwrite the existing tag data.

Example
-------

`REACH:10`

The race has a reach of ten feet.

**.MOD Example:**

Initial Race: `<race name> <tab> REACH:5`

Modified By: `<race name>.MOD <tab> REACH:10`

Is Equivalent To: `<race name> <tab> REACH:10`

The final reach is "10".

