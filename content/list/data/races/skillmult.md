+++
date = "2016-08-01"
title = "SKILLMULT (Data: races.lst)"
original_url = "list/data/races.html#skillmult"
categories = [ "all-tag", "races-tag" ]
+++

## Status

None

## Syntax

`SKILLMULT:x`

## Parameters

-   x: Number (Skill Multiplier)



What it does
------------

-   Defines the Multiplier of the skill points when the character is
    first level.
-   Default is x4.
-   Most Multi-hit die creatures have SKILLMULT:1 since adding class
    levels is done as Multi-Classing.
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `SKILLMULT` tag, the data included in a new `SKILLMULT`
    tag will overwrite the existing tag data.

Example
-------

`SKILLMULT:1`

Monsters have x1 since adding class levels is done as Multi-classing.

**.MOD Example:**

Initial Race: `<race name> <tab> SKILLMULT:1`

Modified By: `<race name>.MOD <tab> SKILLMULT:2`

Is Equivalent To: `<race name> <tab> SKILLMULT:2`

The final skill multiplier is "2".

