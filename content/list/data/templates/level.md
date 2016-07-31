+++
date = "2016-08-01"
title = "LEVEL (Data: templates.lst)"
original_url = "list/data/templates.html#level"
categories = [ "all-tag", "templates-tag" ]
+++

## Status

Updated 5.11.11

## Syntax

`LEVEL:x:y:z`

## Parameters

-   x: Number (Level at which the benefit is granted)
-   y: ANY valid Template or Global Token which can
    accept trailing PRE tags can be used
-   z: Number or Text (Must be valid for the tag used)



What it does
------------

-   Grants the character an ability at the level specified.
-   This is the character's total character level.
-   The abilities of these tags have been enhanced so that they can call
    any global tag.\
-   The text may contain the following tags:\
    -   `ABILITY` - [Ability](/list/global/other/ability.html)
    -   `CR` - [Challenge Rating](/list/data/templates/cr.html)
    -   `DR` - [Damage Reduction](/list/global/other/dr.html)
    -   `FEAT` - [Feat](/list/data/templates.html#feat)
    -   `MOVE` - [Move](/list/global/other/move.html)
    -   `SAB` - [Special Ability](/list/global/other/sab.html)
    -   `SR` - [Spell Resistance](/list/global/other/sr.html)
    -   Any valid Template or Global Token which can accept trailing PRE
        tags can also be used
-   This may appear more than once in a template.
-   Feats added by this tag are considered automatic feats and do not
    count against a PC's feat pool.
-   **.MOD Behavior:** When modifying a template with the `.MOD` tag,
    given an existing `LEVEL` tag, the data included in a new `LEVEL`
    tag will be included as if it were a separate tag.

Examples
--------

`LEVEL:1:DR:5/+1`

Grants Damage Reduction of 5/+1 at Level 1.

`LEVEL:2:SR:15`

Grants Spell Resistance of 15 at Level 2.

`LEVEL:3:CR:2`

Grants an increase in Challenge Rating of two at Level 3.

`LEVEL:3:MOVE:Burrow,20`

Grants an a burrowing rate of 20 at Level 3.

`LEVEL:4:SAB:Uncanny Dodge`

Grants the "Uncanny Dodge" special ability at Level 4.

`LEVEL:5:FEAT:Alertness`

Grants the "Alertness" feat at Level 5.

`LEVEL:6:FEAT:TYPE.Fighter`

Produces a popup menu at Level 6 from which a PC can choose a fighter
feat.

`LEVEL:6:ABILITY:FEAT|AUTOMATIC|Empower Spell`

Grants the "Empower Spell" feat as an automatic feat at Level 6.

**.MOD Example:**

Initial Template: `Werewolf <tab> LEVEL:1:DR:5/1`

Modified By: `Werewolf.MOD <tab> LEVEL:2-7:CR:2`

Is Equivalent To: `Werewolf <tab> HD:1:DR:5/1 <tab> HD:2:CR:2` .

The werewolf gains Damage Reduction of "5/1" at Level 1 and is granted
an increase in Challenge Rating of two at Level 2.

