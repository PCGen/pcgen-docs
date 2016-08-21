+++
date = "2016-08-01"
title = "RACE (Global: CHOOSE)"
original_url = "list/global/choose.html#race"
categories = [ "all-tag", "choose-tag" ]
+++

## Status

Updated 6.03.02

## Syntax

`CHOOSE:RACE|x|y|y[x]|y[x,x]|x,y,y[x],y[x,x]`

## Parameters

-   x: Text (Race, by name or key)
-   x: FEAT=Text (Feat, by name or key)
-   x: RACETYPE=Text (Race-type)
-   x: RACESUBTYPE=Text (Race-subtype)
-   x: BASESIZE=Text (Size value)
-   x: TYPE=Text (Race type)
-   x: !TYPE=Text (Prohibited race type)
-   x: ALL
-   y: ANY (Default)
-   y: PC
-   y: QUALIFIED



What it does
------------

-   This will produce a list of all races matching the criteria.
-   Using the `FEAT=Text` sub-tag will provide a list of races selected
    by the referenced feat. The feat referenced must contain a
    `CHOOSE:RACE` tag.
-   Using the `RACETYPE=Text` sub-tag will provide a list of races
    selected by the referenced race-type. The referenced race-type is
    defined in the race's `RACETYPE` tag.
-   Using the `RACESUBTYPE=Text` sub-tag will provide a list of races
    selected by the referenced race-subtype. The referenced race-subtype
    is defined in the race's `RACESUBTYPE` tag.
-   Using the `BASESIZE=Text` sub-tag will provide a list of races
    selected by the referenced size as defined in the <span
    class="lstfile"> sizeAdjustment.lst </span> gameMode file. The size
    referenced will be compared to the base size, e.i. the contents of
    the `SIZE` tag in the **RACE** LST file, and will ignore any
    modifications to the size granted through any means.
-   Global qualifiers work for races. Use of the qualifiers has the
    following effect:
    -   **ANY** - Will return a list of all races.
    -   **PC** - Will return a list of all races already selected by the
        Player Character.
    -   **QUALIFIED** - Will return a list of all races that the player
        character is otherwise qualified for.
-   Qualifiers can be logically negated by prefacing with the
    exclamation point (!), i.e. `!PC` is a valid usage.
-   Criteria can be logically combined by using the comma (,), logical
    **AND** , and the pipe (|), logical **OR** . Logical **AND** s are
    evaluated before logical **OR** s.
-   The [SELECT](/list/global/other/select.html) tag is used in
    conjunction with this `CHOOSE` tag to define the number of
    "selections" that can be made.

Example
-------

`CHOOSE:RACE|RACETYPE=Dragon`

This will produce a list of all races that have the Dragon racial type.

`CHOOSE:RACE|Dwarf|Elf`

This will produce a list of races including only the **Dwarf** and the
**Elf** .

`CHOOSE:RACE|RACETYPE=Humanoid,RACESUBTYPE=Aquatic`

This will produce a list of all Humanoid races that have the Aquatic
subtype.

`CHOOSE:RACE|BASESIZE=M`

This will produce a list of all races that have a size of "M".

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

