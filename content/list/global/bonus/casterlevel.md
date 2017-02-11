+++
date = "2016-08-01"
title = "CASTERLEVEL (Global: BONUS)"
original_url = "/list/global/bonus.html#casterlevel"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "CASTERLEVEL"
    parent = "global_bonus"
    identifier = "global_bonus_CASTERLEVEL"
+++

## Status

Updated 5.7.1

## Syntax

`BONUS:CASTERLEVEL|x|y`

## Parameters

-   x: Text (Class name)
-   x: ALLSPELLS
-   x: DESCRIPTOR.Text (Spell descriptor name)
-   x: DOMAIN.Text (Domain name)
-   x: RACE.Text (Race name)
-   x: SCHOOL.Text (School name)
-   x: SPELL.Text (Spell name)
-   x: SUBSCHOOL.Text (Subschool name)
-   x: TYPE.Text (Class type)
-   y: Number, variable or formula (Number to add to
    caster level)



What it Does
------------

-   Each spellcasting class should have a CASTERLEVEL bonus associated
    with it.
-   If no CASTERLEVEL bonus is present for a spell casting class, it
    will default to class level.
-   The [CASTERLEVEL](/list/data/spells/casterlevel.html) tag is only
    used in spell.lst lines for DESC, DURATION and TARGETAREA tags.
-   This BONUS statement can be used to increase just these
    output items.
-   This BONUS statement will NOT increase spells known or spell slots.
    You must use [BONUS:PCLEVEL](/list/global/bonus/pclevel.html)
    for that.
-   This BONUS statement can be used to set the caster level of innate
    racial spells.

Examples
--------

`BONUS:CASTERLEVEL|Sorcerer|1`

Adds 1 to Sorcerer spell caster level.

`BONUS:CASTERLEVEL|TYPE.Arcane|1`

Adds 1 to Arcane spell caster level.

`BONUS:CASTERLEVEL|RACE.Gelfling|4`

Sets Gelfling innate racial spell caster level to 4.

`BONUS:CASTERLEVEL|SPELL.Levitate|2`

Adds 2 to caster level for the 'Levitate' spell.

`BONUS:CASTERLEVEL|SCHOOL.Transmutation|2`

Adds 2 to caster level for all spells of the 'Transmutation' school.

`BONUS:CASTERLEVEL|Paladin|CL/2|PRECLASSLEVEL:Paladin=4`

Sets the Paladin's spell caster level to half his class level after he
reaches level 4.

(Note that the syntax used in this last example is only valid in a class
line)

`CLASS:Defender.MOD <tab> SPELLSTAT:INT <tab> BONUSSPELLSTAT:NONE <tab> SPELLTYPE:Arcane <tab> SPELLBOOK:NO <tab> BONUS:CASTERLEVEL|Defender|TL <tab> SPELLLIST:1|Channeler`

Modifying the class Defender changes all of these tags to determine
bonus spells and maximum casting level.

**Additional qualifier:** .RESET

.RESET is an additional qualifier that can be used for all subtags
except CLASS and RACE. What .RESET does is resets the caster level to
the value specified instead of adding it to PC's caster level (which is
what would usually be done). Note that if any .RESET qualifier is
encountered then the caster level is reset even if other bonus tags do
not have them. Also, multiple .RESET encountered do not overwrite each
other.

The syntax is: `BONUS:CASTERLEVEL|subtag.text.RESET|number`

Examples using .RESET
---------------------

`CASTERLEVEL|TYPE.Divine.RESET|max(CASTERLEVEL.TOTAL,10)`

In this example all Divine spells would have a caster level of either 10
or the PC's default caster level, whichever is higher.

`BONUS:CASTERLEVEL|SPELL.Fireball.RESET|7`

`BONUS:CASTERLEVEL|SCHOOL.Evocation.RESET|3`

These two bonuses in combination would result in a caster level of 10
for Fireball (because it is also in the school of Evocation) and 3 for
all other Evocation spells

