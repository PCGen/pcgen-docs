+++
date = "2016-08-01"
title = "RACETYPE (Data: races.lst)"
original_url = "/list/data/races.html#racetype"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "RACETYPE"
    parent = "data_races"
    identifier = "data_races_RACETYPE"
+++

## Status

None

## Syntax

`RACETYPE:x`

## Parameters

-   x: Text (Creature Type)



<span id="racetype"></span> \*\*\* New 5.9.4

What it does
------------

-   Defines the Type of creature the race is.
-   A Creature may only have one RACETYPE at any given time.
-   The Base RACETYPE set in the race line can be changed with a
    RACETYPE tag in a template or other file type.
-   Currently existing selections from the Monster List include:
    Aberration, Animal, Beast, Construct, Dragon, Elemental, Fey, Giant,
    Humanoid, Magical Beast, Monstrous Humanoid, Ooze, Outsider, Plant,
    Shapechanger, Undead, and Vermin.
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `RACETYPE` tag, the data included in a new `RACETYPE`
    tag will overwrite the existing tag data.

Example
-------

`RACETYPE:Outsider`

The race is of the "Outsider" type.

`Bugbear (Shadowkind).MOD <tab> OUTPUTNAME:Bugbear <tab> RACETYPE:Humanoid <tab> RACESUBTYPE:Shadowkind <tab> TEMPLATE:Shadowkind <tab> LEVELADJUSTMENT:2`

This modification of the race Bugbear, changes all of the indicated
tags.

**.MOD Example:**

Initial Race: `<race name> <tab> RACETYPE:Humanoid`

Modified By: `<race name>.MOD <tab> RACETYPE:Outsider`

Is Equivalent To: `<race name> <tab> RACETYPE:Outsider`

The race is now of the "Outsider" type.

