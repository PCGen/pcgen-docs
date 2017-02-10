+++
date = "2016-08-01"
title = "LEGS (Data: races.lst)"
original_url = "/list/data/races.html#legs"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "LEGS"
    parent = "data_races"
+++

## Status

None

## Syntax

`LEGS:x`

## Parameters

-   x: Number (Number of Legs)



What it does
------------

-   Used to determine encumbrance and carrying capacity for
    creatures/characters with a nonstandard amount of legs. (i.e. more
    than/less than 2).
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `LEGS` tag, the data included in a new `LEGS` tag will
    overwrite the existing tag data.

Examples
--------

`LEGS:4`

A horse has 4 legs.

`LEGS:0`

Slime and ooze creatures/characters would have no legs!

**.MOD Example:**

Initial Race: `<race name> <tab> LEGS:2`

Modified By: `<race name>.MOD <tab> LEGS:4`

Is Equivalent To: `<race name> <tab> LEGS:4`

The race now has 4 legs.

