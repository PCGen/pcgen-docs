+++
date = "2016-08-01"
title = "Lesson #8: .lst - Biosettings"
original_url = "/list/lst-file-class/08-biosettings.html"

[menu.main]
    identifier = "lst-file-class_08-biosettings"
    name = "Lesson #8: .lst - Biosettings"
    parent = "lst-file-class"
    
+++
By Professor Chris Chandler (Barak).

**File(s) Covered:** \*biosettings.lst

**Tags used:**

`      AGESET          ,           RACENAME          ,           BASEAGEADD          ,           CLASS          ,           SEX          ,           BASEHT          ,           HTDIEROLL          ,           BASEWT          ,           WTDIEROLL          ,           TOTALWT          ,           BASEAGE          ,           MAXAGE          ,           AGEDIEROLL          ,           HAIR          ,           EYES          ,           SKINTONE     `

------------------------------------------------------------------------

**`AGESET`**

The first tag you will see in a biosetting file is the AGESET tag. These
tags are used to define the age ranges for each category. It takes the
format of AGESET:\#|name. The numbers should start with 0 (for the
youngest ageset) and go up sequentially from there for each grouping you
have. So if your game starts at adulthood, your first ageset tag would
probably look like this:

> `AGESET:0|Adult`

One other thing may appear in the AGESET line, and that would be BONUS
tags where you enter any modifiers that affect the character's ability
scores due to age. A good example of this would be the next set up the
age line when you hit Middle Age. The AGESET line for that age group
looks like this:

> `AGESET:1|Middle Age <tab>            BONUS:STAT|STR,CON,DEX|-1 <tab>            BONUS:STAT|INT,WIS,CHA|1`

When you choose middle age or change your age to where it falls in the
middle age category on the description tab in the UI these bonuses and
penalties (-1 to Strength, Dexterity and Constitution and +1 to
Intelligence, Wisdom and Charisma) will be applied to your character.

------------------------------------------------------------------------

**`RACENAME`**

Under the Ageset tag will be the first RACENAME tag. This is used to
define the race (or races) that the rest of the information on the
racename line will affect. You may have multiple RACENAME lines with the
same name as long as they contain different types of information (more
on this later). As a matter of fact, other than the AGESET tag, this is
the only other tag that may begin a line in a biosettings .lst file.

The way that a RACENAME line can be made to affect multiple races is by
use of the "%" character with the name, which acts as a wildcard
character. We use this when there is a race with sub-races that all have
the same progressions and effects as they age. A couple of examples:
RACENAME:Dwarf (would affect only races with the name of "Dwarf").
"RACENAME:Dwarf%" would affect any race that started with the word
Dwarf, so "Dwarf (Duergar)" would also be affected by whatever
information follows this RACENAME tag.

------------------------------------------------------------------------

**`BASEAGEADD`**

The BASEAGEADD tag is used inside of the CLASS tag to define the spread
for randomization in the number that is added to your base age for the
class(es) it is paired with.

It takes the format of \[BASEAGEADD:\#d\#\]. The standard practice
(since that's how it's done in most books) is to notate this in standard
dice format. 1d4 would generate a random number between 1 and 4 to add
to the base age, 3d8 would generate a number between 3 and 24 to add to
the base age, etc.

It is possible to enter it such that the full range would be covered
(say 1-24 instead of 3-24). To do this you would simply change the entry
to 1d24 and it will generate a random number between 1 and 24 to add to
the character's base age.

------------------------------------------------------------------------

**`CLASS`**

The CLASS tag is somewhat complicated to explain, especially because it
embeds one of the other tags we'll be discussing within it. We use this
tag to define the names of the classes that affect the age of the
character and how much should be added to their base age for the class
they've chosen. There will only be one RACENAME/CLASS line combo for
each race represented in the biosetting file.

The CLASS tag takes the format of

CLASS:class name1,class name2\[BASEAGEADD:\#d\#\]|class name3,class
name4\[BASEAGEADD:\#d3\]|etc.

So, from the SRD, for a Human the RACENAME/CLASS line would look like:

> `RACENAME:Human% <tab>            CLASS:Barbarian,Rogue,Sorcerer[BASEAGEADD:1d4]|Bard,Fighter,Paladin,Ranger[B ASEAGEADD:1d6]|Cleric,Druid,Monk,Wizard[BASEAGEADD:2d6]`

------------------------------------------------------------------------

**`BASEHT`**

The BASEHT tag is used inside of the SEX tag to define the starting
point for the height of the race. There will normally be two of these
for each race. One for the female and one for the male.

It takes the format of BASEHT:\#. This number needs to be in the base
units set in the game mode. If you set the base unit to the centimeter
then a race with a starting height of 160 centimeteres would have
BASEHT:160. If you set it for meters, it would be BASEHT:1.6.

------------------------------------------------------------------------

**`HTDIEROLL`**

The HTDIEROLL tag is used inside of the SEX tag to define the spread for
randomization in the number that is added to your base height for the
race/sex it is paired with. It also acts as a variable name that
contains the result of this randomization.

It takes the format of HTDIEROLL:\#d\#. This is usually expressed in
standard dice notation (2d6, 3d4, etc.) but like the other randomization
tags, you can get the full range by using expressions like 1d12, etc.

------------------------------------------------------------------------

**`BASEWT`**

The BASEWT tag is used inside of the SEX tag to define the starting
point for the weight of the race. There will normally be two of these
for each race. One for the female and one for the male.

It takes the format of BASEWT:\#. Like the BASEHT, this number needs to
be in the base units set in the game mode for it to output properly.

------------------------------------------------------------------------

**`WTDIEROLL`**

The WTDIEROLL tag is used inside of the SEX tag to define the spread for
randomization in the number that is added to your base weight for the
race/sex it is paired with. It also acts as a variable name that
contains the result of this randomization.

It takes the format of WTDIEROLL:\#d\#. This is usually expressed in
standard dice notation (2d6, 3d4, etc.) but like the other randomization
tags, you can get the full range by using expressions like 1d12, etc.

------------------------------------------------------------------------

**`TOTALWT`**

The TOTALWT tag is used inside of the SEX tag to define the total weight
of your character. It can use standard numbers, as well as the BASEWT,
WTDIEROLL and HTDIEROLL variables.

An example of the use of this tag from the SRD for the human race is
TOTALWT:BASEWT+(HTDIEROLL\*WTDIEROLL). It would set your total weight to
the value of your base weight, plus the product of the random height and
weight rolls.

------------------------------------------------------------------------

**`SEX`**

This tag uses the previous five tags listed above to define the height
and weight of a character based on their sex. The tag takes the format
of SEX:&lt;gender&gt;\[sub-tags\]&lt;gender&gt;\[sub-tags\]. The
sub-tags are separated by pipes within the brackets.

An example (again from the SRD):

> `RACENAME:Human%            SEX:Male[BASEHT:58|HTDIEROLL:2d10|BASEWT:120|WTDIEROLL:2d4|TOTALWT:BASEWT+(HTDIEROLL*WTDIEROLL)]Female[BASEHT:53|HTDIEROLL:2d10|BASEWT:85|WTDIEROLL :2d4|TOTALWT:BASEWT+(HTDIEROLL*WTDIEROLL)]`

------------------------------------------------------------------------

**`BASEAGE`**

This tag sets the bottom of the AGESET it is listed under. The format is
BASEAGE:\#. This number also controls the change in bonuses if you set
your characters age manually. If you go below this number, it removes
the current bonus for the AGESET you were in and applies the previous
AGESET bonus statements.

For a race that starts a certain ageset at 35 years, you would see:

> `BASEAGE:35`

------------------------------------------------------------------------

**`MAXAGE`**

This tag sets the top of the AGESET it is listed under. The format is
MAXAGE:\#. This number also controls the change in bonuses if you set
your characters age manually. If you go above this number, it removes
the current bonus for the AGESET you were in and applies the next AGESET
bonus statements.

For a race that ends a certain ageset at 55 years, you would see:

> `MAXAGE:55`

------------------------------------------------------------------------

**`AGEDIEROLL`**

This tag sets the randomization scale for the AGESET it is under. The
format is AGEDIEROLL:\#d\#.

Standard practice is to try and fill the range between the BASEAGE value
and the MAXAGE value in dice notation. So for the values of those given
above we see the we need a range of 20, so our tag would look like:

> `AGEDIEROLL:1d20`

------------------------------------------------------------------------

**`HAIR`**

This tag determines the hair colors used by the randomizer. It takes the
format of HAIR:color1|color2|color3|etc. Any text you wish may be used
as a hair color.

> `RACENAME:Human% <tab> EYES:Hazel|Blue|Brown|Grey|Violet`

------------------------------------------------------------------------

**`SKINTONE`**

This tag determines the skintone colors used by the randomizer. It takes
the format of SKINTONE:color1|color2|color3|etc. Any text you wish may
be used as a skintone color.

> `RACENAME:Human% <tab> SKINTONE:Bronze|Yellow|Red|Pink|Vermillion`

Note that the last six may be combined on the same RACENAME line (and
usually are) like so:

> `RACENAME:Human% <tab> HAIR:Blonde|White|Salt & Pepper|Plaid            EYES:Hazel|Blue|Brown|Grey|Violet            SKINTONE:Bronze|Yellow|Red|Pink|Vermillion`

After the first ageset where you set all the other randomization
information, the other agesets are entered. The only things contained in
these areas should be AGESET (and associated BONUS statements),
RACENAME, BASEAGE, MAXAGE and AGEDIEROLL. And example from the SRD would
be:

> `AGESET:1|Middle Age BONUS:STAT|STR,CON,DEX|-1            BONUS:STAT|INT,WIS,CHA|1            RACENAME:Human% BASEAGE:35 MAXAGE:52 AGEDIEROLL:3d6            RACENAME:Dwarf% BASEAGE:125 MAXAGE:187 AGEDIEROLL:(7d8+1d6)            RACENAME:Elf% BASEAGE:175 MAXAGE:262 AGEDIEROLL:11d8            RACENAME:Gnome% BASEAGE:100 MAXAGE:149 AGEDIEROLL:(8d6+1)            RACENAME:Half-Elf% BASEAGE:62 MAXAGE:92 AGEDIEROLL:5d6            RACENAME:Half-Orc% BASEAGE:30 MAXAGE:44            AGEDIEROLL:(1d10+1d4)            RACENAME:Halfling% BASEAGE:50 MAXAGE:74 AGEDIEROLL:4d6`

------------------------------------------------------------------------

Well now.... isn't that a monster dissertation?!!! I hope everyone finds
it helpful in creating biosettings files for whatever sources you choose
to work on. Between this lesson and the examples in the PCGen
distribution you should have it made.

Best of luck!

Barak\
 LST Chimp



