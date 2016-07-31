+++
date = "2016-08-01"
title = "RACESUBTYPE (Data: templates.lst)"
original_url = "list/data/templates.html#racesubtype"
categories = [ "all-tag", "templates-tag" ]
+++

## Status

New 5.9.4

## Syntax

`RACESUBTYPE:x|x`

## Parameters

-   x: Text (Creature Subtype)
-   x: .REMOVE.Text (Removes Creature Subtypes)



What it does
------------

-   Adds or removes additional Subtypes to the creature.
-   Initial Subtypes are defined by the
    [RACESUBTYPE](/list/data/races/racesubtype.html) race tag.
-   Examples include: Air, Angel, Aquatic, Archon, Augmented, Chaotic,
    Cold, Earth, Evil, Extraplanar, Fire, Goblinoid, Good, Incorporeal,
    Lawful, Native, Reptilian, Shapechanger, Swarm, Water as well as
    Humaniod subraces such as Elf, Orc, Dwarf, etc..
-   .MOD Behavior: When modifying a template, with the `.MOD` tag, given
    an existing `RACESUBTYPE` tag, the data included in a new
    `RACESUBTYPE` tag will be appended to the existing tag data.

Example
-------

`RACESUBTYPE:Lawful|Air`

Adds the "Lawful" and "Air" subtypes.

`RACESUBTYPE:.REMOVE.Evil`

Removes the "Evil" subtype.

`RACESUBTYPE:.REMOVE.Extraplanar|Native`

Removes the "Extraplanar" subtype and adds "Native" subtype.

**.MOD Example:**

Initial Template: `Ooze Monkey <tab> RACESUBTYPE:Simian`

Modified By: `Ooze Monkey.MOD <tab> RACESUBTYPE:Gooey`

Is Equivalent To: `Ooze Monkey <tab> RACESUBTYPE:Simian|Gooey` .

The character is granted the race types "Simian" and "Gooey".

