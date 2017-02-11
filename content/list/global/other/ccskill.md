+++
date = "2016-08-01"
title = "CCSKILL (Global: OTHER)"
original_url = "/list/global/other.html#ccskill"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "CCSKILL"
    parent = "global_other"
    identifier = "global_other_CCSKILL"
+++

## Status

None

## Syntax

`CCSKILL:x|x`

## Parameters

-   x: Text (&lt;Skill Name&gt;)
-   x: Text (Type.&lt;Skill Type&gt;)
-   x: LIST



What it does
------------

Grants the listed exclusive skills as cross-class skills.

Examples
--------

`CCSKILL:Listen|Spot`

The "Listen" and "Spot" skills are made cross-class skills.

`CCSKILL:Search|TYPE.Knowledge`

The "Search" and "Knowledge" type skills are made cross-class skills.

`CCSKILL:LIST`

Skills selected in the associated choice are made cross-class skills.

`CLASS:Blackguard.MOD <tab> STARTSKILLPTS:2 <tab> CSKILL:.CLEAR|Handle Animal|Ride <tab> CSKILL:Concentration|TYPE.Craft|Diplomacy|Heal|Intimidate|Knowledge (Religion)|TYPE.Profession|Climb|Jump|Listen|Spot|Swim|Pilot <tab> CCSKILL:Handle Animal|Ride`

Modified Class that changes all of these Tags from their starting
values..

