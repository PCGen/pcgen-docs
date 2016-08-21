+++
date = "2016-08-01"
title = "Lesson #13: .lst - Feats (Part 2 - prerequisites)"
original_url = "/list/lst-file-class/13-feat-2.html"

[menu.main]
    identifier = "lst-file-class_13-feat-2"
    name = "Lesson #13: .lst - Feats (Part 2 - prerequisites)"
    parent = "lst-file-class"
    
+++
By Professor Chris Chandler (Barak)

File(s) Covered: \*feat.lst

Tags used/discussed:

EQ, GT, LT, NEQ, GTEQ, LTEQ, [PREALIGN](/list/global/pre/prealign.html)
, [PREATT](/list/global/pre/preatt.html) ,
[PRECHECK](/list/global/pre/precheck.html) ,
[PRECHECKBASE](/list/global/pre/precheckbase.html) ,
[PRECLASS](/list/global/pre/preclass.html) ,
[PREEQUIP](/list/global/pre/preequip.html) ,
[PREFEAT](/list/global/pre/prefeat.html) ,
[PREITEM](/list/global/pre/preitem.html) ,
[PRELEVEL](/list/global/pre/prelevel.html) ,
[PRELEVELMAX](/list/global/pre/prelevelmax.html) ,
[PREMOVE](/list/global/pre/premove.html) ,
[PREMULT](/list/global/pre/premult.html) ,
[PRERACE](/list/global/pre/prerace.html) ,
[PRESIZE](/list/global/pre/presize.html) ,
[PRESKILL](/list/global/pre/preskill.html) ,
[PRESPELLTYPE](/list/global/pre/prespelltype.html) ,
[PRESTAT](/list/global/pre/prestat.html) ,
[PRETEXT](/list/global/pre/pretext.html) ,
[PREVAR](/list/global/pre/prevar.html)

This tutorial will cover the use of prerequisite tags (which we refer to
as PRExxx tags in general) in feats as they relate to actually
qualifying for the feat. They may also be used to limit the application
of the benefits of the feat, but that usage will be discussed in the
tutorial on the BONUS tags at a later time.

As with the CHOOSE tag from the previous tutorial, there are \*many\*
PRExxx tags. I will cover some of the ones I believe you might commonly
see/use, but for a full listing and syntax rules, you should browse the
PRExxx section of the documentation included with PCGen.

A few general notes in regards to using PRExxx tags in feats:

1\) To be a feat PRExxx (used to qualify you to actually take the feat
itself) it must \*not\* be attached to another tag.

2\) You may put as many PRExxx tags on a feat line as you want and
\*all\* must be met before the feat can be taken (unless the feat is
granted by a tag that allows the user to bypass PRExxx tags, such as the
VFEAT tag).

3\) You may use PRExxx attached to other tags within the feat to control
what bonuses are applied and where and when, but they will not be used
in the determination of whether or not you can take the feat itself.
While VFEAT will bypass PRExxx tags for the taking of the feat, the ones
attached to other tag will still be active.

4\) The general format of a PRExxx tag is either PRExxx:\#,y=z,y=z for
those that compare something to a number or PRExxx:\#,z,z for those that
do not compare to a number.; The \# determines how many of the y=z pairs
(or z specs) you must qualify for to be considered as having met the
prereq. Although, as with almost everything in life, there are
exceptions.

5\) In the documentation, some of these tags are referred to as "Global".
This means that they are supposed to work in any file type (feat,
template, spell, etc.) \*NOT\* that they will work with any tag. This is
an important distinction. If a tag is not documented as being able to
have PRExxx tags applied, then it most likely will not function if you
try to do so.

6\) When a PRExxx tag is doing a comparison with a number, it is assumed
to be met if equal to or greater than in most instances. Those tags that
do not function this way have suffixes (explained further below) that
modify the comparison behavior.

7\) Any PRExxx tag may be prefixed with a "!" character (!PRExxx) in
order to invert the requirement. The PRExxx tag will be evaluated as
normal, then the result reversed (meaning you CAN NOT have the things
listed in this tag) when determining whether the prerequisite is passed
or not.

------------------------------------------------------------------------

**EQ, NEQ, GT, LT, GTEQ, LTEQ**

There are several tags that do comparisons other than the normal
"greater than or equal to" that is the standard. In these cases there
are suffixes that get attached to the tag to tell it what type of
comparison is desired to make it evaluate as true. Those tags that these
suffixes go with will not function without them, so make sure and note
which tags use them.

The suffixes and their meanings are:

> EQ - &gt; Equal\
>  NEQ -&gt; Not Equal\
>  LT -&gt; Less Than\
>  LTEQ -&gt; Less Than or Equal\
>  GT -&gt; Greater Than\
>  GTEQ -&gt; Greater Than or Equal

So when in use you would basically see "&lt;base tag&gt;EQ" or "&lt;base
tag&gt;LTEQ:", and that is the condition that must be satisfied for that
PRExxx tag to be evaluated to true.

I will note which tags take these suffixes when I cover them below.

------------------------------------------------------------------------

**PREALIGN**

This tag is one of the exceptions mentioned above to the standard PRExxx
format rule. This one takes the format of
PREALIGN:&lt;align1&gt;,align&lt;2&gt;,etc. To pass this PRExxx you need
only meet one of the listed criteria.

You may use number or text representations for the alignments. The
identifiers for the alignments are as follows:

> 0 or LG = Lawful Good\
>  1 or LN = Lawful Neutral\
>  2 or LE = Lawful Evil\
>  3 or NG = Neutral Good\
>  4 or TN = True Neutral\
>  5 or NE = Neutral Evil\
>  6 or CG = Chaotic Good\
>  7 or CN = Chaotic Neutral\
>  8 or CE = Chaotic Evil\
>  9 or None = None\
>  10 or Deity = Deity's alignment

**Examples:**

`PREALIGN:LG,CG`

Must be Lawful Good or Chaotic Good alignment

`PREALIGN:Deity`

Character's alignment must match that of their chosen deity.

------------------------------------------------------------------------

**PREATT**

This tag checks the value of the characters Base Attack Bonus (the
attack bonuses granted from class advancement and race). If the
character's BAB is equal to or greater than the number given the PRExxx
is met.

This is another tag that does not follow the standard format. It takes
the form of PREATT:\#.

**Example:**

`PREATT:3`

Characters BAB must be 3 or greater

------------------------------------------------------------------------

**PRECHECK/PRECHECKBASE**

These tags compare the value of the check(s)/saving throw(s) against the
number(s) you supply in the tag and if the value of the check is equal
to or higher than the prereq value given, the prereq is considered to be
met.

The PRECHECKBASE compares the base save (defined in game play as the
total from classes... in program terms, it will add in anything defined
by BONUS:CHECKS|BASE.&lt;checkname&gt;|\#). The PRECHECK compares the
total (which would include bonuses from items, stats, etc.) of the check
to the given number.

The check/save to be checked \*must\* be one of the ones defined in your
gamemode files or the tag will fail.

**Examples:**

`PRECHECKBASE:1,Fortitude=1,Reflex=3`

Would evaluate as true if the character's base Fortitude meets or
exceeds 5 or their base Reflex meets or exceeds 3

`PRECHECK:2,Fortitude=2,Will=2,Reflex=2`

Would evaluate as true if any 2 of the 3 three listed conditions were
met.

------------------------------------------------------------------------

**PRECLASS**

This tag is used to check class levels, and whether the character meets
or exceeds the specified level(s). The general format is
PRECLASS:\#,&lt;classparameter&gt;=&lt;level&gt;.

You can reference the classes in several ways; by explicit name, type
(TYPE.Base, TYPE.PC, TYPE.Monster, TYPE.Prestige, etc), whether the
character has spellcasting levels in general (SPELLCASTER) or of a
specific type (SPELLCASTER.Arcane or SPELLCASTER.Divine).

**Example:**

`PRECLASS:1,Fighter=3`

Must have three levels in the Fighter class

`PRECLASS:2,TYPE.Prestige=1,SPELLCASTER=3`

Must have one Prestige level and three levels in a spellcasting class

`PRECLASS:1,SPELLCASTER.Arcane=1`

Must have one level in an arcane casting class

------------------------------------------------------------------------

**PREEQUIP**

This PRExxx checks for equipment items that you have equipped. It will
ignore items that are not set as "equipped".

The format for this tag is
PREEQUIP:\#,&lt;itemspecifier&gt;,&lt;itemspecifier&gt;,etc. The item
may be specified by name or by type (which refers to the TYPE tag used
in the equipment definition file). If you use the name option you may
use a wildcard (the % symbol) in it.

You may also specify the item by it's wield category (by using
WIELDCATEGORY=... this basically referring to weapons). You may use any
wield category that is defined in the game mode files.

**Examples:**

`PREEQUIP:1,Longsword`

Must have an item with the exact name "Longsword equipped.

`PREEQUIP:2,TYPE=Armor,TYPE=Shield`

Must have both a piece of equipment with "Armor" contained in its TYPE
tag and one with "Shield" contained in its TYPE tag equipped.

`PREEQUIP:1,WIELDCATEGORY=OneHanded`

Must have a weapon equipped that has a wield category of One Handed.

------------------------------------------------------------------------

**PREFEAT**

Used to check for the character having the specified feats (or not
having them when reversed. This tag is used very frequently, so it would
be advisable to learn this one well.

This tag has a slightly different format in that there are not x=y
pairs. The basic format is PREFEAT:x,y,z. The x is the number of feats
(or instances of the same feat in certain circumstances) that the
character must have. Y is an optional parameter called "CHECKMULT" that
makes the tag count each instance of a feat that can be taken multiple
times separately. For example: if you do not use the CHECKMULT tag and
are checking for the Spell Focus feat and the character had it in three
different schools, it would only count as one feat. Z would be the feat
parameters themselves.

This tag also has a special option to allow you to specify that the
character \*doesn't\* have a certain feat (while still specifying that
they do have others). This is done by enclosing the feat specification
in brackets.

The feat specifications can be done either by the feat name or the feat
type. For feats that have choices, you can specify the general feat
only, or a certain specific version of it by adding the specific choice
in parentheses following the feat name (with no space in between).

**Examples:**

`PREFEAT:1,Dodge,Combat Reflexes`

Must have the Dodge feat or the Combat Reflexes feat

`PREFEAT:2,TYPE=Fighter`

Must have two feats with a type of Fighter

`PREFEAT:2,CHECKMULT,Spell Focus`

Must have any two Spell Focus feats

`PREFEAT:1,Spell Focus(Evocation)`

Must have Spell Focus in the Evocation school

`PREFEAT:2,CHECKMULT,Spell Focus,[Spell Focus(Evocation)`

Must have two Spell Focus feats, and \*not\* have Spell Focus(Evocation)

------------------------------------------------------------------------

**PREITEM**

This PRExxx checks for items in a characters possession. Note that these
items do not have to be equipped or carried, they must just appear in
the characters inventory.

It has the general format of PREITEM:\#,&lt;itemparameter&gt;. The item
may be specified by name or by type (which refers to the TYPE tag used
in the equipment definition file). If you use the name option you may
use a wildcard (the % symbol) in it.

**Examples:**

`PREITEM:1,Longsword`

`Must have an item named "Longsword"`

`PREITEM:1,Longsword %`

Must have an item that has Longsword as the beginning of the name. This
would match "Longsword +1" and "Longsword (Soulstealer)" but not
"Soulstealer Longsword"

`PREITEM:2,Longsword,Shortsword`

Must have a "Longsword" and a "Shortsword"

`PREITEM:2,TYPE=Sword,TYPE=Sword`

Must have two different items that have "Sword" in the TYPE tag of their
.lst definition

------------------------------------------------------------------------

**PRELEVEL**

This tag checks for the total number of class levels. Note that it
includes monster hit dice and levels.

The format is PRELEVEL:\#, where \# represents the total number of
levels the character must meet or exceed to pass the PRExxx.

**Examples:**

`PRELEVEL:4`

Character must have at least four levels between all class levels,
monstrous hit dice or monstrous class levels.

------------------------------------------------------------------------

**PRELEVELMAX**

This tag sets the maximum level. It only counts character (non-monster)
levels. To meet the PRExxx you must be of the specified character level
or lower.

A special note about this token: when used as a PRExxx for a feat you
will not be allowed to take the feat after the specified level, but as
long as you take the feat before you reach that level you will still
receive the benefits of the feat even after you are above the level
specified (however, it \*will\* show in red on your feat list in the
GUI).

**Examples:**

`PRELEVELMAX:3`

Character may not have more than three character (class) levels

------------------------------------------------------------------------

**PREMOVE**

This tag checks that the character meets or exceeds the specified
types/rates of movement specified. It takes the format of
PREMOVE:\#,&lt;movementtype&gt;=&lt;movementrate&gt;,etc.

**Examples:**

`PREMOVE:1,Climb=10,Brachiate=10`

Character must have a Climb movement rate of 10' or more or a Brachiate
movement rate of 10' or more

`PREMOVE:2,Walk=30,Fly=30`

Character must have both a Walk movement rate of 30' and a Fly movement
rate of 30'

------------------------------------------------------------------------

**PREMULT**

This tag in itself does not check anything. It is used to allow the
combination of different types of PRExxx tags into one. This helps cover
those options where you have a PRExxx that states "Must have the Dodge
feat or Dex of 15" (that "or" in there is the kicker that couldn't be
handled prior to this tag being created).

This tag may also be nested within itself.

The tag takes the following format:
PREMULT:\#,\[&lt;PRExxx&gt;\],\[&lt;PRExxx&gt;\]. The number is the of
the other bracketed PRExxx conditions you need to meet.

**Examples:**

`PREMULT:1,[PREFEAT:1,Dodge],[PRESTAT:1,DEX=15]`

Must have the Dodge feat or a Dex of 15

`PREMULT:1,[PREMULT:2,[PREATT:3],[PRESTAT:1,STR=15]],[PREFEAT:1,CombatExpertise]`

Must have Strength of 15 and a base attack bonus of 3 \*OR\* have the
Combat Expertise feat

------------------------------------------------------------------------

**PRERACE**

This tags can check for a characters race, race type (as defined by the
TYPE tag), racial type (as defined by the RACETYPE tag), or racial
subtype (as defined by the RACESUBTYPE tag).

Using this PRExxx you can do things such as checking for Incorporeal
Undead, Giants, etc.

There are a couple of special additions for this tag. First, as in a few
other tags you may use the % symbol as a wildcard. Second, if you wish
to exclude a race, you may put square brackets around it.

**Examples:**

`PRERACE:1,Dwarf`

Must be a Dwarf

`PRERACE:2,RACETYPE=Undead,RACESUBTYPE=Incorporeal`

Must have both a race type of "Undead" and a subtype of "Incorporeal"

`PRERACE:1,RACETYPE=Giant`

Must have a race type of "Giant"

`PRERACE:1,Elf%,[Elf (High)]`

Must be one of the "Elf" races, except "Elf(High)".

------------------------------------------------------------------------

**PRESIZE**

This tag checks the characters current size. It is one of the tags that
I wrote about in the introduction that requires a suffix (EQ, GTEQ, LT,
etc). So what you would actually see in the .lst files would be
"PRESIZEGTEQ" or "PRESIZELT", etc.

The one oddity to this tag is that it does not compare to a number but
to a letter representing the different sizes. Those letters are (and in
order from least to greatest):

> F = Fine\
>  D = Diminutive\
>  T = Tiny\
>  S = Small\
>  M = Medium\
>  L = Large\
>  H = Huge\
>  G = Gargantuan\
>  C = Colossal

The format for this PRExxx is a nonstandard one. It is
PRESIZE&lt;suffix&gt;:&lt;sizeidentifier&gt;

**Examples:**

`PRESIZEEQ:L`

MUst be Large size

`PRESIZEGTEQ:H`

Must be of Huge size or greater

------------------------------------------------------------------------

**PRESKILL**

This tag checks that a characters ranks in the specified skill(s) are
equal to or greater than the specified number.

The tag is in a non-standard format. It looks like this:
PRESKILL:\#,&lt;skillspecifier&gt;,&lt;skillspecifier&gt;=\#. You may
specify the skills by exact name or by TYPE.

**Examples:**

`PRESKILL:1,Spot=10`

Must have ten ranks in the Spot skill

`PRESKILL:1,Spot,Listen=10`

Must have ten ranks in the Spot or Listen skill

`PRESKILL:2,TYPE.Perform,Perform (Dance)=5`

Must have 5 ranks in Perform (Dance) and 5 ranks in one other skill with
"Perform" in the TYPE tag

------------------------------------------------------------------------

**PRESPELLTYPE**

This tag is used to check the characters spellcasting ability.

You may specify that it be in divine casting classes, arcane casting
classes, or psionic and you specify how many of spells of a certain
level are required. You may use "Arcane|Divine" in the &lt;spelltype&gt;
slot to specify Arcane \*or\* divine.

This tag is not in any of the standard formats. It looks like this:
PRESPELLTYPE:&lt;spelltype&gt;,&lt;numberofspells&gt;,&lt;spelllevel&gt;.

**Examples:**

`PRESPELLTYPE:Arcane,2,3`

Must know at least two third level Arcane spells

`PRESPELLTYPE:Divine,1,4`

Must know at least one fourth level Divine spell

------------------------------------------------------------------------

**PRESTAT**

This tag checks the character to make sure they have the specified
ability score equal to or greater than the number specified.

The tag takes the format of
PRESTAT:\#,&lt;statabbrev&gt;=\#,&lt;statabbrev&gt;=\#. You may use any
ability that is defined in the statsandchecks.lst file from the game
mode you are in. The ability/stat is specified in the PRESTAT tag using
the three letter abbreviation for it that is defined in the above
mentioned game mode file.

**Examples:**

`PRESTAT:1,STR=15`

Must have a strength of at least 15

`PRESTAT:2,STR=12,DEX=13`

Must have a strength of 12 or more \*and\* a dexterity of 13 or more

`PRESTAT:1,INT=12,WIS=12`

Must have an intelligence of 12 or more \*or\* a wisdom of 12 or more

------------------------------------------------------------------------

**PRETEXT**

This is a unique PRExxx tag in that it doesn't check for anything. :)

It is used to show a requirement that is (usually) not a game mechanic
and hence not coded into PCGen so that it can be checked. Anything put
in this tag will be displayed in the PCGen GUI so the user knows what
the requirement is, but beyond that it will not prevent the user from
taking the feat or template.

The format it simply PRETEXT:&lt;text&gt;

**Examples:**

`PRETEXT:Must be a member of the Church of the Ninja Monkey`

------------------------------------------------------------------------

**PREVAR**

This tag checks the value of program or user created variables. It is
one of the tags that I wrote about in the introduction that requires a
suffix (EQ, GTEQ, LT, etc). So what you would actually see in the .lst
files would be "PREVARGTEQ" or "PREVARLT", etc.

This is one of the most commonly used PRExxx tags in .lst files. It can
be used to check the values of any of the computer generated variables
(these are usually indicated by being entirely capitalized), such as
SPELLFAILURE and HP. For a list of all the computer generated variables,
see the documentation for the DEFINE tag. It may also be used to check
the value of any variable defined by the user via a DEFINE tag in the
dataset (distinguished by having the first letter of each word
capitalized with no spaces in between).

It takes the format of
PREVAR&lt;suffix&gt;:&lt;varname&gt;,&lt;value&gt;

**Exmples:**

`PREVARLT:SPELLFAILURE,10`

Spell failure must be less than ten

`PREVARGTEQ:RageTimes,2`

RageTimes variable must be two or more

`PREVARGT:TurnUndeadTimes,2,SneakAttack,3`

TurnUneadTimes variable must be greater than two \*and\* SneakAttack
variable must be greater than 3

------------------------------------------------------------------------

With that, I've gone on in this lesson long enough. :p

To bring us back to our feat topic, I will add the required PRExxx for
the Improved Critical feat.

"Prerequisite: Proficient with weapon, base attack bonus +8". We dealt
with the proficiency requirement in our CHOOSE statement (it offers only
weapons you are proficient with) so we can leave that one out, which
leaves the base attack bonus of 8. If you look up a ways you'll see we
need to use the PREATT tag. So it would be "PREATT:8".

For quick reference, we currently have the following for our feat so far
(new lines should tab characters):

> `Improved Critical            TYPE:General.Fighter            PREATT:8            MULT:YES            STACK:NO            CHOOSE:WEAPONPROFS|LIST|1            DESC:With your selected weapon you know how to hit where it hurts.            BENEFIT:When using the weapon you selected, your threat range is doubled.            SOURCELONG:Revised (v.3.5) System Reference Document            SOURCESHORT:RSRD            SOURCEWEB:http://www.wizards.com/default.asp?x=d20/article/srd35            SOURCEPAGE:Feats.rtf`

The next tutorial up will be a discussion of BONUS tags (and in there
the use of PRExxx tags with them).

Barak\
 LST Chimp



