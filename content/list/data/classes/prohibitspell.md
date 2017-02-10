+++
date = "2016-08-01"
title = "PROHIBITSPELL (Data: classes.lst)"
original_url = "/list/data/classes.html#prohibitspell"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "PROHIBITSPELL"
    parent = "data_classes"
+++

## Status

None

## Syntax

`PROHIBITSPELL:x`

## Parameters

-   x: ALIGNMENT.Text (Alignment name)
-   x: DESCRIPTOR.Text (Descriptor name)
-   x: SCHOOL.Text (School name)
-   x: SUBSCHOOL.Text (Subschool name)
-   x: SPELL.Text (Spell name)



<span id="prohibitspell"></span> \*\*\* Updated 5.11.6

What it does
------------

-   Prohibits characters from using certain spells.
-   Alignment, descriptor, school, and subschool names are
    period-delimited (.) lists of the appropriate parameter.
-   Spell name is a comma-delimited (,) list of individual spell names.
-   Alignment restrictions imposed by this tag can be turned off by the
    PROHIBITSPELLS house rule preference.
-   This tag can be qualified with PRExxx statements using a pipe (|) as
    the delimiter.

Example
-------

`PROHIBITSPELL:ALIGNMENT.Evil`

Prohibits the character from taking spells with the "Evil" descriptor.

`PROHIBITSPELL:ALIGNMENT.Chaotic.Evil`

Prohibits the character from taking spells that have both the "Chaotic"
and the "Evil" descriptors.

`PROHIBITSPELL:DESCRIPTOR.Fear`

Prohibits the character from taking spells with the "Fear" descriptor.

`PROHIBITSPELL:SCHOOL.Illusion`

Prohibits the character from taking spells from the "Illusion" school.

`PROHIBITSPELL:SUBSCHOOL.Healing`

Prohibits the character from taking spells from the "Healing" subschool.

> `1 <tab> PROHIBITSPELL:ALIGNMENT.Good|PREALIGN:LE,NE,CE <tab> PROHIBITSPELL:ALIGNMENT.Evil|PREALIGN:LG,NG,CG <tab> PROHIBITSPELL:ALIGNMENT.Lawful|PREALIGN:CG,CN,CE <tab> PROHIBITSPELL:ALIGNMENT.Chaotic|PREALIGN:LG,LN,LE <tab> PROHIBITSPELL:ALIGNMENT.Good|PREDEITYALIGN:LE,NE,CE <tab> PROHIBITSPELL:ALIGNMENT.Evil|PREDEITYALIGN:LG,NG,CG <tab> PROHIBITSPELL:ALIGNMENT.Lawful|PREDEITYALIGN:CG,CN,CE <tab> PROHIBITSPELL:ALIGNMENT.Chaotic|PREDEITYALIGN:LG,LN,LE`

Prohibits the character from taking "Good" spells if alignment is
LE,NE,CE; taking "evil" spells if alignment is LG,NG,CG; taking "Lawful"
spells if alignment is CG,CN,CE; taking "Chaotic" spells if alignment is
LG,LN,LE; taking "Good" spells if Deity alignment is LE,NE,CE; taking
"evil" spells if Deity alignment is LG,NG,CG; taking "Lawful" spells if
Deity alignment is CG,CN,CE; taking "Chaotic" spells if Deity alignment
is LG,LN,LE.

`PROHIBITSPELL:SPELL.Fireball,Lightning Bolt`

Prohibits the character from taking either "Fireball" or "Lightening
Bolt" spells.

Where it is used
----------------

Class Line and Class Level Line.

