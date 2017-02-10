+++
date = "2016-08-01"
title = "FACE (Data: races.lst)"
original_url = "/list/data/races.html#face"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "FACE"
    parent = "data_races"
    identifier = "data_races_FACE"
+++

## Status

None

## Syntax

`FACE:x,y`

## Parameters

-   x: Number (Space the creature occupies)
-   y: Number (Optional, side space)



What it does
------------

-   Describes how much space the creature takes up. For 3.0 rules this
    tag is used for the Face statistic. For 3.5 rules this tag is used
    for the Space statistic. If only one number is used it is assumed to
    represent all sides.
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `FACE` tag, the data included in a new `FACE` tag will
    overwrite the existing tag data.

Example
-------

`FACE:5,10`

The race has a face of 5 by 10.

`FACE:10`

The race has a face of 10.

**.MOD Example:**

Initial Race: `<race name> <tab> FACE:10`

Modified By: `<race name>.MOD <tab> FACE:5,10`

Is Equivalent To: `<race name> <tab> FACE:5,10`

The race now has a face of 5 by 10.

