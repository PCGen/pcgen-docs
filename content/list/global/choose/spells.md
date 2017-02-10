+++
date = "2016-08-01"
title = "SPELLS (Global: CHOOSE)"
original_url = "/list/global/choose.html#spells"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "SPELLS"
    parent = "global_choose"
+++

## Status

New - 5.13.x

## Syntax

`CHOOSE:SPELLS|x,y,y[z]|x|y|y[z;z]`

## Parameters

-   x: Text (Spell name)
-   x: TYPE=Text (Spell type)
-   x: SCHOOL=Text (Spell school)
-   x: SUBSCHOOL=Text (Spell subschool)
-   x: DESCRIPTOR=Text (Spell descriptor)
-   x: PROHIBITED=Boolean (Optional)
-   x: SPELLBOOK=Text (Spellbook name)
-   y: CLASSLIST=Text (Class name)
-   y: DOMAINLIST=Text (Domain name)
-   y: SPELLTYPE=Text (Spell type)
-   y: ALL
-   z: KNOWN=Boolean (Optional)
-   z: LEVELMIN=Number, Variable, Formula, or
    MAXCASTABLE (Minimum spell level, Optional)
-   z: LEVELMAX=Number, Variable, Formula, or
    MAXCASTABLE (Maximum spell level, Optional)



What it does
------------

-   Presents a list of spells matching the criteria defined by the
    included sub-tags.
-   The `PROHIBITED` sub-tag will restrict the presented spell list to
    prohibited ("YES") spells or non-prohibited ("NO") spells. If it is
    not included, both are presented.
-   The `SPELLBOOK` sub-tag is used to reference the specific spell
    book, such as "Innate", in which the spells is located.
-   The spell type used in the `SPELLTYPE` sub-tag above MUST be used in
    a `SPELLTYPE` tag within a loaded class.
-   The `KNOWN` sub-tag will restrict the presented spell list to
    known ("YES") spells or unknown ("NO") spells. If it is not
    included, both are presented.
-   The `LEVELMIN` sub-tag references all spells of the specified level
    and higher within the context of the "y" variable preceding
    the brackets.
-   The `LEVELMAX` sub-tag references all spells of the specified level
    and lower within the context of the "y" variable preceding
    the brackets.
-   The "z" variable **MUST** be contained within a set of
    square-brackets (\[ \]) and paired with a single "y" variable. Only
    one set of square brackets per "y" variable is allowed.
-   Independent "z" parameters require the use of multiple sets of
    square brackets (\[ \]), one for each "z" parameter paired with is
    own "y" parameter. (e.g. y\[z\]|y\[z\])
-   Dependent "z" parameters can use a common set of square-brackets
    (\[ \]) paired with the associated "y" parameter. (e.g. y\[z;z\])
-   **Note:** y\[z;z\]|y\[z\] is legal, y\[z\]\[z\] is not.
-   The [SELECT](/list/global/other/select.html) tag is used in
    conjunction with this `CHOOSE` tag to define the number of
    "selections" that can be made.

Example
-------

`CHOOSE:SPELLS|Acid Arrow|Magic Missile|Ray of Frost`

Choose between Acid Arrow, Magic Missile and Ray of Frost

`CHOOSE:SPELLS|CLASSLIST=Psion[LEVELMIN=1;LEVELMAX=3]`

Choose from Psion spells between first level and third level

`CHOOSE:SPELLS|SPELLTYPE=Arcane,SCHOOL=Evocation`

Choose from Arcane Evocation spells

`CHOOSE:SPELLS|DESCRIPTOR=Good`

Choose from spells with the Good descriptor

`CHOOSE:SPELLS|ALL[KNOWN=YES]`

Choose from spells known by the PC.

`CHOOSE:SPELLS|ALL[LEVELMAX=MAXCASTABLE-1],SPELLTYPE=Arcane`

Choose from spells that are both up to the maximum castable (of any
spell) level minus 1 AND `SPELLTYPE=Arcane` .

`CHOOSE:SPELLS|CLASSLIST=Sorcerer[LEVELMIN=1;LEVELMAX=MAXCASTABLE-1]`

Choose from Sorcerer spells between first level and one less than your
max castable level of spell taken from the Sorcerer list

`CHOOSE:SPELLS|SPELLTYPE=Psionic[KNOWN=YES]|SPELLTYPE=Psionic[LEVELMAX=MAXCASTABLE-1]`

Choose from any Psionic "Spell" known by the PC or available to any
Psionic Caster at a level at least one less than the maximum level of
Psionic "Spell" castable by the PC. Notice the independence of the
`KNOWN` and `LEVELMAX` subtags forces the use of two sets of square
brackets (\[ \]).

`CHOOSE:SPELLS|SPELLTYPE=Psionic[KNOWN=YES;LEVELMAX=MAXCASTABLE-1]`

Choose from any Psionic "Spell" known by the PC at a level at least one
less than the maximum level of Psionic "Spell" castable by the PC.
Notice the common case between the `KNOWN` , `LEVELMIN` , and `LEVELMAX`
subtags can be done with one set of square brackets (\[ \]).

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

