+++
date = "2016-08-01"
title = "SKILL (Global: BONUS)"
original_url = "/list/global/bonus.html#skill"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "SKILL"
    parent = "global_bonus"
+++

## Status

Updated 5.7.14

## Syntax

`BONUS:SKILL|x,x|y`

## Parameters

-   x: Text (Skill name)
-   x: STAT.Text (Stat name)
-   x: TYPE=Text (Skill type)
-   x: LIST
-   x: ALL
-   y: Number, variable or formula (Number to add to
    skill level)



What it Does
------------

-   Adds bonus to skills matchng the listed criteria.
-   When the `STAT` subtag is used this will add to skills based on the
    listed stat.
-   When the `TYPE` subtag is used this will add to skills of the
    listed type.
-   The `LIST` subtag is used in conjunction with a `CHOOSE` tag and
    will add to skills chosen.
-   There is no leading space between the comma groups.

Note: Don't forget the space in subsets (i.e. between Craft and
(Metalworking),Craft (Metalworking))

Example
-------

`BONUS:SKILL|Bluff,Listen|10`

Adds 10 to "Bluff" & "Listen".

`BONUS:SKILL|TYPE=Charisma|2`

Adds 2 to Charisma type skills.

`BONUS:SKILL|Spot|5|!PRESKILL:1,Spot=1`

Gain a +5 bonus to Spot, provided you have zero ranks in Spot.

`BONUS:SKILL|Hide|1|TYPE=Talent.STACK`

Adds 1 to Hide skill due to Talent and does Stack with all other Talent
type.

`Balance.MOD <tab> BONUS:SKILL|Balance|max(0,floor((var("SKILLRANK=Tumble")-5)/20))*SynergyBonus|TYPE=Synergy.STACK`

Modifies the Balance skill to include the Synergy Bonus.

`BONUS:SKILL|STAT.STR|1`

Adds one to all "Strength" based skills.

`BONUS:SKILL|LIST|2`

Adds a +2 bonus, to a skill selected by a [`CHOOSE:SKILL`
tag](/list/global/choose/skill.html) . The word `LIST` is a placeholder
for the skill chosen by the player.

`CHOOSE:SKILLSNAMEDTOCSKILL|2 <tab> BONUS:SKILL|LIST|6|TYPE=Legendary`

Adds six to the two selected Class Skills skill learned during Legendary
Class.

`BONUS:SKILL|ALL|1`

Adds one to all skills.

`TEMPBONUS:ANYPC|SKILL|Hide|min(floor((%CHOICE+3)/4)*10,30)|TYPE=Competence <tab> CHOOSE:NUMBER|MIN=1|MAX=20|TITLE=Choose spell caster level`

A chooser that figures your hide % (I think) 1 to 20 points in
Casterlevel, you figure out the math.

