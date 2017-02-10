+++
date = "2016-08-01"
title = "MONSTERCLASS (Data: races.lst)"
original_url = "/list/data/races.html#monsterclass"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "MONSTERCLASS"
    parent = "data_races"
    identifier = "data_races_MONSTERCLASS"
+++

## Status

None

## Syntax

`MONSTERCLASS:x:y`

## Parameters

-   x: Text (Monster Class Name)
-   y: Number (Starting Level)



What it does
------------

-   Determines the number of Monster Levels the race gets on start.
-   Class must be TYPE:Monster and have a PRERACETYPE that matches
    the race.
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `MONSTERCLASS` tag, the data included in a new
    `MONSTERCLASS` tag will overwrite the existing tag data.

Example
-------

`MONSTERCLASS:Outsider:2`

The race has 2 levels of Outsider to start.

**.MOD Example:**

Initial Race: `<race name> <tab> MONSTERCLASS:2`

Modified By: `<race name>.MOD <tab> MONSTERCLASS:4`

Is Equivalent To: `<race name> <tab> MONSTERCLASS:4`

The creature's new monster class is "Outsider" with "4" levels.

