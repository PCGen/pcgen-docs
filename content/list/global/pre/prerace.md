+++
date = "2016-08-01"
title = "PRERACE (Global: PRErequisite)"
original_url = "/list/global/pre.html#prerace"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PRERACE"
    parent = "global_pre"
    identifier = "global_pre_PRERACE"
+++

## Status

Updated 5.9.5

## Syntax

`PRERACE:x,y,y`

## Parameters

-   x: Number (The number of racial properties which
    must be met).
-   y: Text (The name of a race).
-   y: TYPE=Text (The name of a race type defined by
    the race TYPE tag).
-   y: RACETYPE=Text (The name of a race type defined
    by the race RACETYPE tag).
-   y: RACESUBTYPE=Text (The name of a race subtype
    defined by the race RACESUBTYPE tag).



What it does
------------

The character must be one of the listed races or possess one of the
racial properties.

TYPE=&lt;Text&gt; can be used to check types set by the race TYPE tag.

RACETYPE=&lt;Race Type&gt; can be used to check racial types such as
Humanoid, Giant and Outsider.

RACESUBTYPE=&lt;Race Subtype&gt; can be used to check racial subtypes
such as Air, Evil and Extraplanar.

The wildcard character (%) can be used to include any text, for example
Elf% will include any race name which begins with Elf. Without the
wildcard character the race name must match exactly.

Enclosing a selection in square brackets (\[ \]) excludes a race.
Brackets do not work for the TYPE, RACETYPE and RACESUBTYPE properties.

TYPE.xxx for reference, TYPE=xxx for assignment.

Examples
--------

`PRERACE:1,Dwarf,Elf,Human`

Character must be a "Dwarf", "Elf" or "Human".

`PRERACE:1,Elf%,[Elf (aquatic)]`

Character must be one of the "Elf" races, except "Elf (aquatic)".

`PRERACE:1,TYPE=Dire`

Character's race type must be "Dire".

`PRERACE:1,RACETYPE=Giant`

Character's race type must be "Giant".

`!PRERACE:1,RACETYPE=Outsider`

Character's race type must not be "Outsider".

`PRERACE:1,RACESUBTYPE=Incorporeal`

Character must have the "Incorporeal" subtype.

`PRERACE:2,RACETYPE=Undead,RACESUBTYPE=Incorporeal`

Character must have both a race type of "Undead" and a subtype of
"Incorporeal".

`PRERACE:1,%`

This will pass if any race has been chosen but will fail if no race has
been selected.

`!PRERACE:1,%`

This will pass if no race has been selected.

`PRERACE:TYPE=Humanoid`

This will pass if a humanoid race has been selected.

`CLASS:Sorcerer.MOD <tab> !PRERACE:Human`

This will pass if no Human race has been selected.

