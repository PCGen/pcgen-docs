+++
date = "2016-08-01"
title = "Lesson #18: .lst - Converting HD and LEVEL template tags"
original_url = "/list/lst-file-class/18-hd-level-conversion.html"

[menu.main]
    identifier = "lst-file-class_18-hd-level-conversion"
    name = "Lesson #18: .lst - Converting HD and LEVEL template tags"
    parent = "lst-file-class"
    
+++
By Professor Eddy Anthony (MoSaT).

**File(s) Covered:** \*template.lst

**Tags used:**

`      HD          ,           LEVEL          ,           PREHD          ,           PRELEVEL          ,           PREPCLEVEL          ,           CR          ,           DR          ,           SA          ,           SAB          ,           SR          ,           ABILITY          ,           BONUS:DR          ,           BONUS:MISC|CR          ,           BONUS:MISC|SR     `

The template tags HD and LEVEL are used in templates to grant a
character feats and abilities at specific levels based on the
character's total levels and are independent of any specific character
classes. The HD tag is counted against levels of Monster Classes and the
LEVEL tag is counted against the character's total levels from all
classes. Both the HD and LEVEL tags provide the following functions:
granting Damage Reduction, granting additions to Challenge Rating and
Spell Resistance, granting Special Abilities and granting automatic
feats.

Both of these tags have been around a long time and have been
problematic at times in the past. Recently much work has been done to
standardize the tags used in PCGen LST and these two tags stand out for
not following the more recent preferred syntax. For these reasons these
two tags will likely be deprecated in the future, as of version 5.14
they are still valid but may be deprecated in the 5.15 line.

Fortunately as of version 5.14 all the functions provided by these tags
can be replicated with other tags using the latest syntax. This page
will show you how to convert each existing use of HD and LEVEL using
different tags with newer syntax.

------------------------------------------------------------------------

### HD and LEVEL Syntax

At its core the HD and LEVEL tags are an older form of PRExxx tags, the
HD tag is a prerequisite for a specified number of monster levels and
the LEVEL tag is a prerequisite for the number of total levels the
character has. Both of these tags can be expressed with this syntax:

`<Prerequisite>:<levels specified>:<Object granting tag>:<Object to be granted>`

The more modern syntax which replaces this can be expressed in this way:

`<Object granting tag>:<Object to be granted>|<Prerequisite>:<levels specified>`

The function of the HD tag is replaced by the prerequisite tag
[PREHD](/list/global/pre/prehd.html) and the function of the LEVEL tag
is replaced by the prerequisite tag
[PRELEVEL](/list/global/pre/prelevel.html) . All of the ranges that can
be specified by the HD and LEVEL tags can be replicated with the syntax
that PREHD and PRELEVEL use as well as a good deal more because of the
flexibility these tags have. For example:

`HD:2+` is now `PREHD:MIN=2`

`HD:5-7` is now `PREHD:MIN=5,MAX=7`

`HD:1-10` is now `PREHD:MAX=10`

The same syntax applies to LEVEL and PRELEVEL. In addition there is now
a [PREPCLEVEL](/list/global/pre/prepclevel.html) tag which is a
prerequisite for the number of non-monster levels the character has.
This is quite useful if you need a prerequisite based on the number of
character levels the character has regardless of the number of racial
hitdice. This is commonly used to regulate feats which can only be taken
at first level with PREPCLEVEL:MAX=1, if PRELEVEL:MAX=1 were used then
an Ogre with no character class levels would not qualify because it has
more than 1 level total even though they are all monster class levels.

------------------------------------------------------------------------

### CR (Challenge Rating)

All Characters have a CR value which is initially set by the CR tag in
the race line. A CR tag by itself in a template will add to this value.
HD:x:CR:y and LEVEL:x:CR:y will both add to the CR value at the levels
specified. BONUS:MISC|CR|x can be used to replace this function in both
HD and LEVEL

`HD:2+:CR:3` is now `BONUS:MISC|CR|3|PREHD:MIN=2`

`HD:1-10:CR:2` is now `BONUS:MISC|CR|2|PREHD:MAX=10`

`LEVEL:5-7:CR:5` is now `BONUS:MISC|CR|5|PRELEVEL:MIN=5,MAX=7`

Keep in mind that CR is additive and there can be several way to express
things, for example a template containing:

`HD:1-3:CR:2 <tab> HD:4-6:CR:3 <tab> HD:7+:CR:4`

Can be converted most literally as:

`BONUS:MISC|CR|2|MAX=3 <tab> BONUS:MISC|CR|3|PREHD:MIN=4,MAX=6 <tab> BONUS:MISC|CR|4|PREHD:MIN=7`

But can also be converted more economically as:

`CR:2 <tab> BONUS:MISC|CR|1|PREHD:MIN=4 <tab> BONUS:MISC|CR|1|PREHD:MIN=7`

------------------------------------------------------------------------

### DR (Damage Reduction)

DR granted by the HD or LEVEL tags can also be handled directly by the
[DR](/list/global/other/dr.html) tag and the
[BONUS:DR](/list/global/bonus/dr.html) tag since these both take PRExxx
tags. There are two aspects to these tags which need to be kept in mind,
the first is that the DR tag does not stack with itself. The second is
that the BONUS:DR tag requires that the character must already have a DR
tag of the kind it will bonus or it will have no effect. This means that
if you have DR:5/Magic and DR:10/Magic from 2 different templates they
will not stack and you will only get the better of the two (in this case
10/Magic). It also means that for the tag BONUS:DR|Magic|2 to have any
effect you must first have a DR:x/Magic tag.

`HD:2+:DR:10/+1` is now `DR:10/+1|PREHD:MIN=2`

`HD:1-10:DR:5/Cold Iron` is now `DR:5/Cold Iron|PREHD:MAX=10`

`LEVEL:5-7:DR:20/Silver` is now `DR:20/Silver|PRELEVEL:MIN=5,MAX=7`

------------------------------------------------------------------------

### FEAT

Feats granted by the HD and LEVEL tags are automatic and do not adjust
the feat pool. Feats granted by the HD and LEVEL tags can be converted
to the ABILITY tag.

`HD:1-10:FEAT:Blind Fight` is now
`ABILITY:FEAT|AUTOMATIC|Blind Fight|PREHD:MAX=10`

`LEVEL:5-7:FEAT:Alertness` is now
`ABILITY:FEAT|AUTOMATIC|Alertness|PRELEVEL:MIN=5,MAX=7`

The FEAT function of HD and LEVEL also supports TYPE.x which will
trigger a pop up window with a list of feats of type x. This is the only
HD and LEVEL function that will trigger a pop up window. The recommended
method to replace this function is to set up an ability pool so the
feats can be manually selected. See Lesson \#17: .lst - [Converting
Feats to
Abilities](/list/lst-file-class/17-converting-feats-to-abilities.html)
for more detailed information on this subject.

------------------------------------------------------------------------

### SA (Special Ability)

The [SA](/list/global/other/sab.html) tag is deprecated, it's
replacement is the [SAB](/list/global/other/sab.html) tag. SA tags
granted with HD and LEVEL should be converted to SAB tags with the
proper PRE tags.

`HD:1-10:SA:Banana toss` is now `SAB:Banana toss|PREHD:MAX=10`

`LEVEL:5-7:SA:Fire in the Hole` is now
`SAB:Fire in the Hole|PRELEVEL:MIN=5,MAX=7`

------------------------------------------------------------------------

### SR (Spell Resistance)

All Characters initially have an SR value of 0 which can then be raised
by the Global SR tag and the BONUS:MISC|SR|x tag. It is not necessary to
have an SR tag raise the value above 0 before you can use
BONUS:MISC|SR|x to raise it further unlike DR and data defined
variables. HD:x:SR:y and LEVEL:x:SR:y will both add to the SR value at
the levels specified. BONUS:MISC|SR|x can be used to replace this
function in both HD and LEVEL

`HD:2+:SR:3` is now `BONUS:MISC|SR|3|PREHD:MIN=2`

`HD:1-10:SR:2` is now `BONUS:MISC|SR|2|PREHD:MAX=10`

`LEVEL:5-7:SR:5` is now `BONUS:MISC|SR|5|PRELEVEL:MIN=5,MAX=7`

Keep in mind that SR is additive and there can be several way to express
things, for example a template containing:

`HD:1-3:SR:2 <tab> HD:4-6:SR:3 <tab> HD:7+:SR:4`

Can be converted most literally as:

`BONUS:MISC|SR|2|MAX=3 <tab> BONUS:MISC|SR|3|PREHD:MIN=4,MAX=6 <tab> BONUS:MISC|SR|4|PREHD:MIN=7`

But can also be converted more economically as:

`SR:2 <tab> BONUS:MISC|SR|1|PREHD:MIN=4 <tab> BONUS:MISC|SR|1|PREHD:MIN=7`

------------------------------------------------------------------------

Eddy\
 LST Chimp



