+++
date = "2016-08-01"
title = "EXCLUSIVE (Data: skills.lst)"
original_url = "/list/data/skills.html#exclusive"
categories = [ "all-tag", "skills-tag" ]
[menu.main]
    name = "EXCLUSIVE"
    parent = "data_skills"
+++

## Status

None

## Syntax

`EXCLUSIVE:x`

## Parameters

-   x: Boolean (YES or NO)



What it does
------------

-   This tells PCGen whether a skill is an exclusive skill or not.
-   If this is set to YES then ONLY classes that have this listed as a
    class skill can take it.
-   The Default is NO.
-   **.MOD Behavior:** When modifying a skill with the `.MOD` tag, given
    an existing `EXCLUSIVE` tag, the data included in a new `EXCLUSIVE`
    tag will overwrite the existing tag data.

Example
-------

`EXCLUSIVE:YES`

This skill may only be taken if it is a class skill.

**.MOD Example (Overwriting):**

Initial Skill: `Brachiation <tab> EXCLUSIVE:YES`

Modified By: `Brachiation.MOD <tab> EXCLUSIVE:NO`

Is Equivalent To: `Brachiation <tab> EXCLUSIVE:NO`

The exclusive skill "Brachiation" is no longer exclusive.

