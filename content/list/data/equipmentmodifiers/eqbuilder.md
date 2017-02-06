+++
date = "2016-08-01"
title = "EQBUILDER (Data: equipment_modifiers.lst)"
original_url = "/list/data/equipmentmodifiers.html#eqbuilder"
categories = [ "all-tag", "equipmentmodifiers-tag" ]
[menu.main]
    name = "EQBUILDER (Data: equipment_modifiers.lst)"
    parent = "equipmentmodifiers"
+++

## Status

None

## Syntax

`CHOOSE:EQBUILDER.SPELL|w|x|y|z`

## Parameters

-   w: Text (Spell Type, i.e. Arcane, Divine, Psionic,
    ANY, optional)
-   x: SCHOOL.Text (School Name, optional)
-   x: SUBSCHOOL.Text (Sub-School Name, optional)
-   x: DESCRIPTOR.Text (Descriptor Text, optional)
-   y: Number (Minimum Level, optional, default 0)
-   z: Number (Maximum Level, optional,
    default MAX\_LEVEL)



<span id="eqbuilder"></span> \*\*\* Updated 5.14.0

What it does
------------

-   Allows the selection of magic/psionic spells/powers by specific
    type, school, sub-school, descriptor, and level, and then adds the
    spell/power to the item being modified.
-   Filtering by multiple types may be done joining several types using
    a comma (,), logocal AND function, or a pipe (|), logical
    OR function.
-   Multiple schools, sub-schools, and descriptors may be logically
    joined by a comma (,), logocal AND function, or a pipe (|), logical
    OR function.
-   Minimum and maximum level of spell may be set by using y and z.

Example
-------

`CHOOSE:EQBUILDER.SPELL|SCHOOL.Enchantment;SUBSCHOOL.Compulsion`

Show all spells that are Evocation AND Compulsion.

`CHOOSE:EQBUILDER.SPELL|SCHOOL.Enchantment|SCHOOL.Abjuration`

Show all spells that are Evocation OR Abjuration.

`CHOOSE:EQBUILDER.SPELL|Arcane,Divine|0|3`

Allows the user to quickly generate a minor scroll

`CHOOSE:EQBUILDER.SPELL|Arcane|SCHOOL.Evocation|0|3`

Allows the user to quickly generate a minor wand with only evocation
spells

`CHOOSE:EQBUILDER.SPELL|Psionics|0|3`

Allows a minor powerstone

`CHOOSE:EQBUILDER.SPELL|Arcane|SCHOOL.Illusion,DESCRIPTOR.Fear|SCHOOL.Abjuration`

Indicates Spells which are: (School Illusion AND Descriptor Fear) OR
School Abjuration

