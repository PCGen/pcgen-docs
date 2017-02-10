+++
date = "2016-08-01"
title = "LEVELADJUSTMENT (Data: races.lst)"
original_url = "/list/data/races.html#leveladjustment"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "LEVELADJUSTMENT"
    parent = "data_races"
+++

## Status

None

## Syntax

`LEVELADJUSTMENT:x`

## Parameters

-   x: Number or Formula (Level Adjustment)



<span id="leveladjustment"></span> \*\*\* Updated 5.11.13

What it does
------------

-   Raises the Effective Character Level (ECL) of the creature by the
    number supplied.
-   This is factored in when determining how much experience is needed
    to raise a character's level. For example, a 1st level character
    with a Level adjustment of 3 would need the same amount of
    experience to reach 2nd level as a 4th level character with no level
    adjustments would need to reach 5th level.
-   The Level Adjustment is added to Monster Hit Dice and/or Character
    Levels to determine the Effective Character Level (ECL) of
    the creature.
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `LEVELADJUSTMENT` tag, the data included in a new
    `LEVELADJUSTMENT` tag will overwrite the existing tag data.

Example
-------

`LEVELADJUSTMENT:1`

Effective Character Level is raised by one.

`Bugbear (Shadowkind).MOD <tab> OUTPUTNAME:Bugbear <tab> RACETYPE:Humanoid <tab> RACESUBTYPE:Shadowkind <tab> TEMPLATE:Shadowkind <tab> LEVELADJUSTMENT:2`

This modification of the race Bugbear, changes all of the indicated
tags.

**.MOD Example:**

Initial Race: `<race name> <tab> LEVELADJUSTMENT:1`

Modified By: `<race name>.MOD <tab> LEVELADJUSTMENT:2`

Is Equivalent To: `<race name> <tab> LEVELADJUSTMENT:2`

Effective Character Level is now raised by two.

