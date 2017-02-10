+++
date = "2016-08-01"
title = "MONCCSKILL (Data: races.lst)"
original_url = "/list/data/races.html#monccskill"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "MONCCSKILL"
    parent = "data_races"
+++

## Status

None

## Syntax

`MONCCSKILL:x|x`

## Parameters

-   x: Text (Skill Name)
-   x: TYPE.Text (Skill Type)



<span id="monccskill"></span> \*\*\* New 5.4

What it does
------------

-   Grants the listed skills as monster cross class skills.
-   The replacement/substitution symbol (%) may be used at the end of
    the skill name.
-   Monster cross class skills are only cross class skills for monster
    classes such as Giant, Outsider, Undead etc.
-   If a monster takes levels in a base class only those skills defined
    as cross class skills in that class count as cross class skills for
    that level, the monster cross class skills will not apply.
-   **.MOD Behavior:** When modifying a race with the `.MOD` tag, given
    an existing `MONCCSKILL` tag, the data included in a new
    `MONCCSKILL` tag will be appended to the existing tag data.

Examples
--------

`MONCCSKILL:Alchemy|Wilderness Lore`

The "Alchemy" and "Wilderness Lore" skills are made monster cross class
skills.

`MONCCSKILL:Alchemy|TYPE.Knowledge`

The "Alchemy" and "Knowledge" type skills are made monster cross class
skills.

**.MOD Example:**

Initial Race: `Ooze Monkey <tab> MONCCSKILL:Alchemy|Wilderness Lore`

Modified By: `Ooze Monkey.MOD <tab> MONCCSKILL:Acrobatics|Stealth`

Is Equivalent To:
`Ooze Monkey <tab> MONCCSKILL:Acrobatics|Alchemy|Stealth|Wilderness Lore`
.

The "Acrobatics", "Alchemy", "Stealth", and "Wilderness Lore" skills are
made monster cross class skills.

