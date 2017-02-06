+++
date = "2016-08-01"
title = "USEUNTRAINED (Data: skills.lst)"
original_url = "/list/data/skills.html#useuntrained"
categories = [ "all-tag", "skills-tag" ]
[menu.main]
    name = "USEUNTRAINED (Data: skills.lst)"
    parent = "skills"
+++

## Status

None

## Syntax

`USEUNTRAINED:x`

## Parameters

-   x: Boolean (efault is YES)



What it does
------------

-   `YES` or `NO` are used to indicate if this skill can be used
    untrained by the character.
-   **.MOD Behavior:** When modifying a skill with the `.MOD` tag, given
    an existing `USEUNTRAINED` tag, the data included in a new
    `USEUNTRAINED` tag will overwrite the existing tag data.

Example
-------

`USEUNTRAINED:NO`

This skill may not be used if untrained.

**.MOD Example (Overwriting):**

Initial Skill: `Brachiation <tab> USEUNTRAINED:NO`

Modified By: `Brachiation.MOD <tab> USEUNTRAINED:YES`

Is Equivalent To: `Brachiation <tab> USEUNTRAINED:YES`

The modified "Brachiation" skill can be used untrained.

