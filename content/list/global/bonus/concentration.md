+++
date = "2016-08-01"
title = "CONCENTRATION (Global: BONUS)"
original_url = "list/global/bonus.html#concentration"
categories = [ "all-tag", "bonus-tag" ]
+++

## Status

New 5.17.7

## Syntax

`BONUS:CONCENTRATION|x|y`

## Parameters

-   x: Text (Class name)
-   x: ALLSPELLS
-   x: DESCRIPTOR.Text (Spell descriptor name)
-   x: DOMAIN.Text (Domain name)
-   x: SCHOOL.Text (School name)
-   x: SPELL.Text (Spell name)
-   x: SUBSCHOOL.Text (Subschool name)
-   x: TYPE.Text (Class type)
-   y: Number, variable or formula (Number to add to
    caster level)



What it Does
------------

-   Adds to the base concentration bonus for spells, both innate racial
    spells and those granted by spellcasting class, per the
    criteria identified.
-   Each spellcasting class will have a concentration check bonus
    associated with it.

**NOTE:** This bonus is defined with the `SPELLBASECONCENTRATION` game
mode tag. If the game mode does not contain a
[SPELLBASECONCENTRATION](/list/system/gamemode-miscinfo/spellbaseconcentration.html)
tag the output tokens,
[SPELLLISTCLASS.y.CONCENTRATION](/outputsheet/tokens/spell.html#spelllist)
and
[SPELLMEM.v.w.x.y.CONCENTRATION](/outputsheet/tokens/spell.html#spellmem)
, will generate an empty string. Output sheets should check the value of
these tokens, and if empty should not display concentration check
bonuses.

Examples
--------

`BONUS:CONCENTRATION|ALLSPELLS|1`

Adds 1 the concentration check bonuses for all spells.

`BONUS:CONCENTRATION|Sorcerer|1`

Adds 1 to Sorcerer spell concentration check bonuses.

`BONUS:CONCENTRATION|TYPE.Arcane|1`

Adds 1 to Arcane spell concentration check bonuses.

`BONUS:CONCENTRATION|SPELL.Levitate|2`

Adds 2 to concentration check bonuses for the 'Levitate' spell.

`BONUS:CONCENTRATION|SCHOOL.Transmutation|2`

Adds 2 to concentration check bonuses for all spells of the
'Transmutation' school.

`BONUS:CONCENTRATION|SPELL.Fireball|2`

Adds 2 to concentration check bonuses for the "Fireball' spell.

