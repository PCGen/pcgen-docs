+++
date = "2016-08-01"
title = "SPELLLEVEL (Global: CHOOSE)"
original_url = "/list/global/choose.html#spelllevel"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "SPELLLEVEL"
    parent = "global_choose"
+++

## Status

Updated 6.3.0

## Syntax

`CHOOSE:SPELLLEVEL|w|x|y|z|x|y|z`

## Parameters

-   w: TITLE=Text (Chooser title. Optional)
-   x: Text (Spellcaster class)
-   x: CLASS=Text (Spellcaster class)
-   x: SPELLTYPE=Text (Spell type)
-   x: TYPE=Text (Class type)
-   x: !TYPE=Text (Class type)
-   x: ALL
-   y: Number or formula (Minimum level)
-   z: Formula (Maximum level)



What it does
------------

-   Display a list of a character's spell levels for the specified class
    or type.
-   `TITLE` provides a descriptive title for the chooser.
-   `CLASS=Text` will include spell levels of the designated classe.
-   `SPELLTYPE=Text` will include spell levels of the designated
    spell type.
-   `TYPE` will include, or exclude in the case of `!TYPE` , spell
    levels of the designated spell type.
-   Levels will only be included if they fall between the range of
    minimum Level (y) and maximum Level (z), inclusive.
-   The [SELECT](/list/global/other/select.html) tag is used in
    conjunction with this `CHOOSE` tag to define the number of
    "selections" that can be made.

Example
-------

`CHOOSE:SPELLLEVEL|CLASS=Wizard|0|MAXLEVEL|SPELLTYPE=Divine|1|3`

Would present a list of the character's castable Wizard levels of spells
(e.g. Wizard 0 Wizard 1 Wizard 2 for a 5th level Wizard) and Cleric 1
Cleric 2 Cleric 3 if the character had Cleric as a class.

`CHOOSE:SPELLLEVEL|SPELLTYPE=Arcane|0|MAXLEVEL <tab> BONUS:SPELLCAST|%LIST|1`

Would present a list of the character's castable Arcane spells and allow
one to be chosen as a bonus spell per day.

Example Conversion to New Syntax
--------------------------------

`CHOOSE:SPELLLEVEL||2|TYPE.Arcane|4|MAXLEVEL+30[BONUS:SPELLCAST|CLASS=%;LEVEL=%|1]`
becomes

`SELECT:2 <tab> CHOOSE:SPELLLEVEL|SPELLTYPE=Arcane|4|MAXLEVEL+30 <tab> BONUS:SPELLCAST|%LIST|1`

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

