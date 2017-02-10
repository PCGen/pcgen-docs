+++
date = "2016-08-01"
title = "ASPECT (Data: feats.lst)"
original_url = "/list/data/feats.html#aspect"
categories = [ "all-tag", "feats-tag" ]
[menu.main]
    name = "ASPECT"
    parent = "data_feats"
+++

## Status

New 5.15.2

## Syntax

`ASPECT:x|y|z|z`

## Parameters

-   x: Text (Name of Aspect)
-   y: Text (Value of Aspect)
-   z: Number or Formula (Optional. Used for
    substitutions in y)



What it does
------------

-   Identifies an "aspect" (see examples below) that a feat has and sets
    it's value.
-   This tag can be used multiple times within a feat but each time it
    must identify a new aspect.
-   The text in the y variable can use %z for replacing numerical values
    set by the z variable, %1 is replaced by the first z, %2 is replaced
    by the second z, etc..
-   The y text can also use other special variables, also usable in the
    `DESC` tag:
    -   `%CHOICE` - Will replace the first associated choice in
        the object.
    -   `%LIST` - Will substitute all choices comma separated into
        that parameter.
    -   `%NAME` - The `OUTPUTNAME` or name of the object this `DESC` tag
        is in.
-   **.MOD Behavior:** When modifying a feat with the `.MOD` tag, given
    an existing `ASPECT` tag, the data included in a new `ASPECT` tag
    will selectively overwrite the existing tag data or include the
    separate tags. Since each aspect name can hold only one value per
    feat, modifying an existing `ASPECT` tag will overwrite only the
    value of the aspect by that name in the feat, and will add a
    separate `ASPECT` tag with a new name.

Example
-------

`ASPECT:Action Type|Standard Action`

Identifies the "Action Type" of an action performed as part of the
associated feat as a "Standard Action".

`ASPECT:Attack Type|Melee weapon`

Identifies the "Attack Type" of an attack performed as part of the
associated feat as a "Melee weapon" attack.

`ASPECT:Target|One creature`

Identifies the "Target" of an action performed as part of the associated
feat as "One creature".

`ASPECT:Attack|Strength vs. AC`

Identifies an "Attack" performed as part of the associated feat as
"Strength vs. AC".

`ASPECT:Attack Type|Ranged %1|PowerRange`

Identifies the "Attack Type" of an attack performed as part of the
associated feat as a "Ranged" attack with a range equivalent to the
"PowerRange" variable.

`ASPECT:Effect|Double damage to %CHOICE creatures`

Identifies the "Effect" of an action performed as part of the associated
feat as "Double damage" to the creature chosen by the associated
chooser.

**.MOD Example (Overwrite):**

Initial Feat: `<feat name> <tab> ASPECT:A1|A2`

Modified By: `<feat name> <tab> ASPECT:A1|A3`

Is Equivalent To: `<feat name> <tab> ASPECT:A1|A3`

**.MOD Example (Include Separately):**

Initial Feat: `<feat name> <tab> ASPECT:A1|A2`

Modified By: `<feat name> <tab> ASPECT:B1|B2`

Is Equivalent To: `<feat name> <tab> ASPECT:A1|A2 <tab> ASPECT:B1|B2`

