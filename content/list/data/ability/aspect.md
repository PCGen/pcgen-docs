+++
date = "2016-08-01"
title = "ASPECT (Data: abilities.lst)"
original_url = "list/data/ability.html#aspect"
categories = [ "all-tag", "ability-tag" ]
+++

## Status

New 5.15.2

## Syntax

`ASPECT:x|y|z|z`

## Parameters

-   x: Text (Name of Aspect)
-   y: Text (Value of Aspect)
-   z: Number or Formula (Substitution value.
    Optional.)



What it does
------------

-   Identifies an "aspect" (see examples below) that an ability has and
    sets its value.
-   PRExxx tags can be used with the `ASPECT` tag.
-   This tag can be used multiple times within an ability but each time
    it must identify a new aspect unless the `ASPECT` tag includes a
    PRExxx tag appended to the end.
-   When using multiple `ASPECT` tags for the same "aspect" and PRExxx
    tags appended to the end of each, the final value for that aspect
    will be set by the physically last `ASPECT` tag in the ability line
    that passes the prerequisite.
-   The text in the (y) parameter can use %\# for substituting numerical
    values set by the (z) parameter, %1 is replaced by the first (z), %2
    is replaced by the second (z), etc..
-   The (y) parameter can also use other special variables as is done in
    the `DESC` tag:
    -   `%CHOICE` - Will replace the first associated choice in
        the object.
    -   `%LIST` - Will substitute all choices comma separated into
        that parameter.
    -   `%NAME` - The `OUTPUTNAME` or name of the object this `DESC` tag
        is in.
-   **.MOD Behavior:** When modifying an ability with the `.MOD` tag,
    given an existing `ASPECT` tag, the data included in a new `ASPECT`
    tag will selectively overwrite the existing tag data or include the
    separate tags. Since each aspect name can hold only one value per
    ability, modifying an existing `ASPECT` tag will overwrite only the
    value of the aspect by that name in the ability, and will add a
    separate `ASPECT` tag with a new name.

Example
-------

`ASPECT:Action Type|Standard Action`

Identifies the "Action Type" of an action performed as part of the
associated ability as a "Standard Action".

`ASPECT:Attack Type|Melee weapon`

Identifies the "Attack Type" of an attack performed as part of the
associated ability as a "Melee weapon" attack.

`ASPECT:Target|One creature`

Identifies the "Target" of an action performed as part of the associated
ability as "One creature".

`ASPECT:Attack|Strength vs. AC`

Identifies an "Attack" performed as part of the associated ability as
"Strength vs. AC".

`ASPECT:Attack Type|Ranged %1|PowerRange`

Identifies the "Attack Type" of an attack performed as part of the
associated ability as a "Ranged" attack with a range equivalent to the
"PowerRange" variable.

`ASPECT:Effect|Double damage to %CHOICE creatures`

Identifies the "Effect" of an action performed as part of the associated
ability as "Double damage" to the creature chosen by the associated
chooser.

`ASPECT:Target|One creature <tab> ASPECT:Target|Two creatures|PREPCLEVEL:MIN=7,MAX=12 <tab> ASPECT:Target|Three creatures|PREPCLEVEL:MIN=13`

Identifies the "Target" of an action performed as part of the associated
ability as "One creature" for characters that are level 1-6, "Two
creatures"' for characters level 7-12, and "'Three creatures" for
characters level 13 or greater.

**.MOD Example (Overwrite):**

Initial Ability:
`CATEGORY=<category name>|<ability name> <tab> ASPECT:A1|A2`

Modified By:
`CATEGORY=<category name>|<ability name> <tab> ASPECT:A1|A3`

Is Equivalent To:
`CATEGORY=<category name>|<ability name> <tab> ASPECT:A1|A3`

**.MOD Example (Include Separately):**

Initial Ability:
`CATEGORY=<category name>|<ability name> <tab> ASPECT:A1|A2`

Modified By:
`CATEGORY=<category name>|<ability name> <tab> ASPECT:B1|B2`

Is Equivalent To:
`CATEGORY=<category name>|<ability name> <tab> ASPECT:A1|A2 <tab> ASPECT:B1|B2`

