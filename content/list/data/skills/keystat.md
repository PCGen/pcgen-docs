+++
date = "2016-08-01"
title = "KEYSTAT (Data: skills.lst)"
original_url = "/list/data/skills.html#keystat"
categories = [ "all-tag", "skills-tag" ]
[menu.main]
    name = "KEYSTAT (Data: skills.lst)"
    parent = "skills"
+++

## Status

None

## Syntax

`KEYSTAT:x`

## Parameters

-   x: Text (Abbreviated name of stat
    from statsandchecks.lst)



What it does
------------

-   This is to set what stat (as defined by the Game Mode List File) the
    skill draws bonuses from.
-   If the tag is not included no Stat bonus will be applied.
-   **.MOD Behavior:** When modifying a skill with the `.MOD` tag, given
    an existing `KEYSTAT` tag, the data included in a new `KEYSTAT` tag
    will overwrite the existing tag data.

Example
-------

`KEYSTAT:INT`

Sets the Key stat for the skill to Intelligence.

**.MOD Example (Overwriting):**

Initial Skill: `Brachiation <tab> KEYSTAT:DEX`

Modified By: `Brachiation.MOD <tab> KEYSTAT:STR`

Is Equivalent To: `Brachiation <tab> KEYSTAT:STR`

The keystat for the skill "Brachiation" is no "Strength".

