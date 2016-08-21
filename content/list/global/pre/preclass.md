+++
date = "2016-08-01"
title = "PRECLASS (Global: PRErequisite)"
original_url = "list/global/pre.html#preclass"
categories = [ "all-tag", "pre-tag" ]
+++

## Status

None

## Syntax

`PRECLASS:x,y=z,y=z`

## Parameters

-   x: Number (The number of classes that must be equal
    to or greater than the numbers specified for the check to succeed).
-   y: Text (Class Name)
-   y: TYPE.Text (Class Type)
-   y: SPELLCASTER.
-   y: SPELLCASTER.Type (Spellcaster Type)
-   y: ANY
-   z: Number (Class Level)



What it does
------------

Sets class requirements.

Example
-------

`PRECLASS:2,Wizard=5,Sorcerer=6,Cleric=7`

Multi-classed character must be at least Wiz5/Sor6, Wiz5/Clr7 or
Sor6/Clr7.

`PRECLASS:1,SPELLCASTER=2`

Character must have 2 levels in any spellcasting class. This encompasses
psionic manifesting classes as well, as PCGen does not treat manifesting
differently from spellcasting. Spellcaster and manifester can be
considered interchangeable.

`PRECLASS:1,SPELLCASTER.Arcane=2`

Character must have 2 levels in any arcane spellcasting class.

`PRECLASS:1,SPELLCASTER.Divine=6,SPELLCASTER.Psionic=3`

Character must have 6 levels in any divine spellcasting class or 3
levels in any psionic manifesting class.

`PRECLASS:2,TYPE.Base=5,TYPE.Prestige=1`

Character must have 5 levels in any Base class and 1 level in any
Prestige class.

`PRECLASS:2,ANY`

Multi-classed character must be at least two Classes.

`PRECLASS:1,ANY`

Character must have 1 level in any class.

`PREMULT:1,[PREFEAT:1,Blood of the Fey],[PRECLASS:1,Fey-Touched=1]`

Character must have 1 level in Fey-Touched class or feat Blood of the
Fey.

`PRECLASS:1,Jack o' the Green=5 !PREFEAT:1,TYPE.LASlipperyEel`

Character must have 5 levels in Jack o' the Green class and not have the
feat LASlipperyEel.

`!PRECLASS:1,SPELLCASTER.Arcane=1`

Character must not have 1 level in SPELLCASTER.Arcane class.

`BONUS:COMBAT|AC|1|PRECLASS:1,Shaper=10`

Character adds 1 to armor class if 10 levels in Shaper Class.

`BONUS:WEAPON|TOHIT|4|TYPE=Luck|PRECLASS:1,Wizard=1,Sorcerer=1`

Character adds 4 to To-Hit from luck if 1 level in either
Wizard/Sorcerer Class.

`BONUS:CASTERLEVEL|Minstrel|CL-3|PRECLASS:1,Minstrel=4`

Character adds CL-3 bonus to Casterlevel if 4 levels in Minstrel Class.

`SA:Damage reduction 1/opposed alignment|PRECLASS:1,Shaper=10`

SA: will fire with 10 levels of Shaper Class.

`SA:Spy|PREMULT:2,[PRECLASS:1,Aradil's Eye=5],[PRECLASSLEVELMAX:1,Aradil's Eye=9]`

SA: will fire with 5 levels of Aradil's Eye Class or not more than 9
levels of Aradil's Eye Class.

