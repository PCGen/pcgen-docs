+++
date = "2016-08-01"
title = "SITUATION (Data: skills.lst)"
original_url = "/list/data/skills.html#situation"
categories = [ "all-tag", "skills-tag" ]
[menu.main]
    name = "SITUATION"
    parent = "data_skills"
    identifier = "data_skills_SITUATION"
+++

## Status

New 6.03.0

## Syntax

`SITUATION:x|x`

## Parameters

-   x: Text (Skill situation)



What it does
------------

-   This is used to set situational skills.
-   **.MOD Behavior:** When modifying a skill with the `.MOD` tag, given
    an existing `SITUATION` tag, the data included in a new `SITUATION`
    tag will appended to the existing tag data.

Example
-------

`Stealth <tab> SITUATION:In Darkness`

Sets the situational skill "Stealth (In Darkness)".

**.MOD Example:**

Initial Skill: `Stealth <tab> SITUATION:In Darkness`

Modified By: `Stealth.MOD <tab> SITUATION:In Caverns`

Is Equivalent To: `Stealth <tab> SITUATION:In Darkness|In Caverns`

Creates the situational skills "Stealth (In Darkness)" and "Stealth (In
Caverns)".

