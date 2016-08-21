+++
date = "2016-08-01"
title = "RACESUBTYPE (Data: races.lst)"
original_url = "list/data/races.html#racesubtype"
categories = [ "all-tag", "races-tag" ]
+++

## Status

None

## Syntax

`RACESUBTYPE:x|x`

## Parameters

-   x: Text (Creature Subtype)



<span id="racesubtype"></span> \*\*\* New 5.9.4

What it does
------------

-   Defines the Subtypes a creature possesses.
-   Additional Subtypes can be added and/or removed with a RACESUBTYPE
    in a template or other file type.
-   Examples include: Air, Angel, Aquatic, Archon, Augmented, Chaotic,
    Cold, Earth, Evil, Extraplanar, Fire, Goblinoid, Good, Incorporeal,
    Lawful, Native, Reptilian, Shapechanger, Swarm, Water as well as
    Humanoid subraces such as Elf, Orc, Dwarf, etc..
-   The `.CLEAR` tag may be used with this tag.
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `RACESUBTYPE` tag, the data included in a new
    `RACESUBTYPE` tag will be appended to the existing tag data.

Example
-------

`RACESUBTYPE:Lawful|Air`

The race possesses the "Lawful" and "Air" subtypes.

`Bugbear (Shadowkind).MOD <tab> OUTPUTNAME:Bugbear <tab> RACETYPE:Humanoid <tab> RACESUBTYPE:Shadowkind <tab> TEMPLATE:Shadowkind <tab> LEVELADJUSTMENT:2`

This modification of the race Bugbear, changes all of the indicated
tags.

`<race>.MOD <tab> RACESUBTYPE:.CLEAR <tab> RACESUBTYPE:Lawful|Air`

This modification clears a race's existing subtypes and replaces it with
the "Lawful" and "Air" subtypes.

**.MOD Example:**

Initial Race: `Ooze Monkey <tab> RACESUBTYPE:Simian`

Modified By: `Ooze Monkey.MOD <tab> RACESUBTYPE:Gooey`

Is Equivalent To: `Ooze Monkey <tab> RACESUBTYPE:Simian|Gooey` .

The character is granted the race types "Simian" and "Gooey".

