+++
date = "2016-08-01"
title = "SPELLS (Global: OTHER)"
original_url = "/list/global/other.html#spells"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "SPELLS"
    parent = "global_other"
+++

## Status

Updated 6.3.0

## Syntax

`SPELLS:s|u|v|w|x,y|x,y|z|z`

## Parameters

-   s: Text (name of spellbook)
-   s: .CLEARALL
-   u: TIMES=ATWILL (Optional)
-   u: TIMES=Number, Formula, or Variable (Cast times
    per unit time, Optional)
-   v: TIMEUNIT=Text (Unit of time. Optional)
-   w: CASTERLEVEL=Number, Formula, or Variable (Sets
    caster level, Optional)
-   x: Text (Spell name)
-   y: Number or Formula (Spell DC, Optional)
-   z: PRExxx tag



What it does
------------

-   This grants the character spell-like abilities.
-   The spellbook name should conform to PCGen's [Standard Spellbook
    Names](/list/lst-standards.html#stdspellname) .
-   `TIMES` is an optional parameter and if not present will default
    to 1.
-   `TIMEUNIT` can be any unit of time, e.g. Day, Week, Month,
    Encounter, etc., but is optional and if not present will default
    to "Day".
-   `CASTERLEVEL` is an optional parameter and if not present will
    default to 1.
-   There should never be more than one `TIMES` and `CASTERLEVEL` tag
    used within a `SPELLS` tag.
-   You can apply PRExxx tags to the `SPELLS` tag.
    -   If a `SPELLS` tag requires multiple PRExxx tags they are
        pipe-delimited ("|").
    -   If a PRExxx tag has pipe-delimiting ("|") within itself, place
        that PRExxx tag in a separate SPELLS tag by itself.
    -   Once one PRExxx tag is reached at the end, all subsequent fields
        must also be PRExxx tags.
    -   PRExxx's apply to the whole tag.
-   Formulas which use commas within them should be encapsulated using
    parentheses "( )".
-   Because the `SPELLS` tag is not associated with any one class the
    variable "CL" will not work in it.
-   Use of `.CLEARALL` will clear all spell-like abilities for
    the character/creature.

Examples
--------

`SPELLS:Innate|TIMES=3|CASTERLEVEL=(max(TL,1))|Acid Arrow,12+CHA|PRESTAT:1,CHA=12`

"Acid Arrow" is granted as an "Innate" spell 3 times per day if the
character has a Charisma score of at least 12. DC is 12+CHA, and the
Caster level is the character's level (minimum 1).

`SPELLS:Innate|TIMES=ATWILL|CASTERLEVEL=TL|Fireball|Cure Light Wounds`

Grants "Fireball" and "Cure Light Wounds" at will with a caster level
equal to your hitdice in the spellbook "Innate"

`SPELLS:Innate|Charm Person,15`

Grants "Charm Person" once per day, first level with a DC of 15 in the
spellbook "Innate"

`SPELLS:Dragon|CASTERLEVEL=18|Death Ward|PRESTAT:1,WIS=20|PREALIGN:LG,NG,CG`

Grants "Death Ward" once per day with a caster level of 18 in spellbook
"Dragon" requiring a Wisdom of 20 and any good alignment.

`SPELLS:Innate|TIMES=5|TIMEUNIT=Week|Wall of Stone`

Grants "Wall of Stone", 5 times per week at 1st level in Spellbook
"Innate".

