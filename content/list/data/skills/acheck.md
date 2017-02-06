+++
date = "2016-08-01"
title = "ACHECK (Data: skills.lst)"
original_url = "/list/data/skills.html#acheck"
categories = [ "all-tag", "skills-tag" ]
[menu.main]
    name = "ACHECK (Data: skills.lst)"
    parent = "skills"
+++

## Status

None

## Syntax

`ACHECK:x`

## Parameters

-   x: DOUBLE
-   x: NO
-   x: NONPROF
-   x: PROFICIENT
-   x: WEIGHT
-   x: YES



What it does
------------

-   This tells PCGen whether any penalties from equipped armor
    are applied.
-   NO - Armor check penalty does not apply (Default).
-   YES - Armor check penalty applies to this skill.
-   PROFICIENT - Armor check penalty applies if the character is not
    proficient in it.
-   DOUBLE - Armor check penalty of double normal applies to this skill.
-   WEIGHT - Weight carried penalty applies to the skill check.
-   **.MOD Behavior:** When modifying a skill with the `.MOD` tag, given
    an existing `ACHECK` tag, the data included in a new `ACHECK` tag
    will overwrite the existing tag data.

Example
-------

`ACHECK:YES`

Armor check penalty applies to this skill.

**.MOD Example (Overwriting):**

Initial Skill: `Brachiation <tab> ACHECK:YES`

Modified By: `Brachiation.MOD <tab> ACHECK:DOUBLE`

Is Equivalent To: `Brachiation <tab> ACHECK:DOUBLE`

The skill "Brachiation" receives a double penalty from equipped armor.

