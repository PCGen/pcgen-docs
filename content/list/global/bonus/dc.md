+++
date = "2016-08-01"
title = "DC (Global: BONUS)"
original_url = "/list/global/bonus.html#dc"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "DC (Global: BONUS)"
    parent = "bonus"
+++

## Status

Updated 5.5.5

## Syntax

`BONUS:DC|x|y`

## Parameters

-   x: SPELL.Text (Spell name)
-   x: ALLSPELLS
-   x: CLASS.Text (Class name)
-   x: DESCRIPTOR.Text (Spell descriptor)
-   x: DOMAIN.Text (Domain name)
-   x: FEATBONUS
-   x: SCHOOL.Text (Spell school)
-   x: SUBSCHOOL.Text (Spell subschool)
-   x: TYPE.Text (Spell type)
-   y: Number, variable or formula (DC increase)



What it Does
------------

-   Adds to the Difficulty Class (DC) of spell(s) by name, class,
    descriptor, domain, school, subschool, or type.
-   Use of ALLSPELLS adds to the DC of all spells.
-   Use of FEATBONUS raises the DC of spells that receive the applied
    feat bonus, i.e. through the application of a metamagic feat, by
    raising the spell level of the affected spells.
-   `%LIST` can be used with this tag to insert a choice made with a
    `CHOOSE` tag.

Example
-------

`BONUS:DC|SPELL.Fireball|7`

Adds 7 to the DC of the spell Fireball.

`CHOOSE:DC|SCHOOLS|ALL <tab> BONUS:DC|SCHOOL.%LIST|1`

Choose 1 School and add 1 to its DC.

`BONUS:DC|ALLSPELLS|1`

Adds 1 to the DC of all spells.

`BONUS:DC|CLASS.Sorcerer|2`

Adds 2 to the DC of sorcerer spells.

`BONUS:DC|DESCRIPTOR.Law|4`

Adds 4 to the DC of any spells with the Law descriptor.

`BONUS:DC|DESCRIPTOR.Law,DOMAIN.Law|3`

Adds 3 to the DC of any spells with the Law domain or descriptor and
would add 6 to a spell with both the Law Domain and Law Descriptor.

`BONUS:DC|DOMAIN.War|6`

Adds 6 to the DC of War Domain spells.

`MULT:YES <tab> CHOOSE:|Air|Earth|Fire|Water <tab> BONUS:DC|DOMAIN.%LIST|1`

Choose a domain and add 1 to the DC of spells for that domain. This may
be used multiple times.

`BONUS:DC|FEATBONUS|1`

Adds 1 to the DC of spells that this bonus applies to by raising the
spell's level by 1. The Heighten Spell metamagic feat is an example of
where this is used.

`BONUS:DC|SCHOOL.Enchantment|2`

Adds 2 to Enchantment school spells.

`MULT:YES <tab> CHOOSE:FEAT=Psionic Focus <tab> BONUS:DC|SCHOOL.%LIST|2|TYPE=Psychic`

Adds 2 to 1 psychic school focus DC.

`BONUS:DC|SCHOOL.Telepathy|SPELLSTAT-CHA|TYPE=Subdiscipline`

Subtracts the Chrisma Modifier to Telepathy School with a bonus type of
"Subdiscipline".

`BONUS:DC|SUBSCHOOL.something|5`

Adds 5 to the any spell with a subschool of "something".

`BONUS:DC|TYPE.Arcane|3`

Adds 3 to arcane spell DCs.

