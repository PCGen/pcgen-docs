+++
date = "2016-08-01"
title = "Lesson #6: .lst - Races (part 4)"
original_url = "/list/lst-file-class/06-race-4.html"

[menu.main]
    identifier = "lst-file-class_06-race-4"
    name = "Lesson #6: .lst - Races (part 4)"
    parent = "lst-file-class"
    
+++
By Professor Chris Chandler (Barak).

**File(s) Covered:** \*races.lst

**Tags used:**

`      MONCSKILL          ,           BONUS:SKILLRANK          ,           BONUS:SKILL          , MFEAT,           CR          ,           PREALIGN          ,           HITDICEADVANCEMENT          ,           LEVELADJUSTMENT          ,           FAVCLASS          ,           LANGAUTO          ,           LANGBONUS          ,           LEGS          ,           HANDS          ,           SPELLS          ,           SOURCEPAGE     `

This will be the final lesson on creating "monster" race files. Once
you've read through this and understand it (and the preceding lessons)
you should not have too much difficulty in creating a monster race file
for PCGen.

With that said, there's a lot of material to be covered, so lets dive
right in.

------------------------------------------------------------------------

**`MONCSKILL`**

To define the skills that are considered class skill for each race we
use the `MONCSKILL` tag.  Following the tag is a list of the race's
class skills, separated by the pipe ("|") character.

To determine a race's class skills, we once again turn to the "Skills"
section of the race's listing (when entering an existing source and not
making up a new race).  Every skill listed there is a class skill for
that race.

The Solar's entry would be:

> `MONCSKILL:Concentration|Escape Artist|Hide|TYPE.Knowledge|TYPE.Craft|Listen|Move Silently|Search|Sense Motive|Spellcraft|Spot`

Note that we have granted ALL Knowledge and Craft skills as racial
skills since they may choose from among all of them.

The entry for the Ninja Monkey will be much shorter.

> `MONCSKILL:Balance|Hide|Jump|Listen|Move Silently|Spot`

**Update to RSRD**\
 The class skills for the Solar in the RSRD are a little different than
in the SRD. The tag in 3.5 would look like:\
 MONCSKILL:Concentration|TYPE.Craft|TYPE.Knowledge|Diplomacy|Escape
Artist|Hide|Listen|Move Silently|Search|Sense Motive|Spellcraft|Spot.\
 Note the neither Survival nor Use Rope are class skills since they are
only listed for skill synergy purposes.\
 The Ninja Monkey is unchanged. It should be noted that Balance **is** a
class skill even though they have no ranks in it since they have a
racial bonus to Balance.

------------------------------------------------------------------------

**`BONUS:SKILLRANK`**

**Note:** The PCGen data team is moving away from using the "Default
Monster" setting.  Default Monster Kits are being used instead.

Now comes another section where we have to work backwards to arrive at
the numbers we need to use.  This would be to determine what ranks the
race gets in each skill.

To begin, we look in the race listing at the "Skills" section.  The
numbers given here are the final numbers  once everything (racial
bonuses, armor/encumbrance, stat modifiers, feats, etc) is taken into
account.  They assume that all equipment listed for the monster is
present and equipped and affecting those physical skills where they
should.

For the Solar, the first skill listed is Concentration.  The final value
should be +16.  We'll begin by subtracting the appropriate stat modifier
(5 from constitution), so we're down to +11.  Looking further, we see no
racial skill modifiers for this skill, no feats that affect it and since
it's not a physical feat equipment would have no effect.  Our tag for
this skill would be:

> `BONUS:SKILLRANK|Concentration|11|PREDEFAULTMONSTER:Y`

Next up is the Escape Artist skill.  The final value needs to be +30.
Subtracting the stat modifier for the skill (5 from dexterity) puts us
at +25.  Once again there are no racial bonuses or feats affecting this
skill. It is physical so we need to check that there are no armor or
encumbrance to affect it.  The two  pieces of equipment for a solar are
it's greatsword and it's longbow.  These are not enough to encumber it,
so there is no effect on the physical skills.  Leaving us with a
skillrank of 25.

Several of the other skills work out to have this value after doing all
the math, and the BONUS:SKILLRANK tag  will let us apply the same bonus
to multiple skills by simply listing them in a comma separated list. 
Our final tag for this skill (and several others) would be:

> `BONUS:SKILLRANK|Escape Artist,Hide,Listen,Move Silently,Sense Motive,Spot|25|PREDEFAULTMONSTER:Y`

Note that a Solar gets a choice of any five craft skills OR any five
knowledge skills.  To let the PCGen user  make these choices, we need to
get a little bit creative.  :)  I've created a set of feats that will
present a chooser for knowledge or craft skills, and after choosing one
it will present a chooser listing all of the  skills of the selected
type and allow them to pick five of them and then assign the appropriate
number of  ranks to those skills.  I use an "
`ADD:FEAT(TYPE=FiveKnowledge22,TYPE=FiveCraft22)` " tag in this race
file to  start the feat chooser.

I will wait to cover the creation of these feats until we go over feat
files, but I wanted to make sure and  mention their use here as the
situation of a race getting a choice of certain skills comes up with
some regularity and you need to know how to deal with it.

For the Ninja Monkey its somewhat simpler.  We just need to determine
how many skill points he should have for  his race type and HD and then
choose what skills he gets ranks in.  According to the MM (pg. 11) A
Monstrous Humanoid should have 2 x Intelligence score +2/EHD.  So the
Ninja Monkey gets 30 skillpoints to spend.

I think I'll give him ranks in Balance, Hide, Jump, Listen, Move
Silently and Spot.  TO keep it simple I'll  just divide the skillranks
equally among these skills.  Our tag would be:

> `BONUS:SKILLRANK|Balance,Hide,Jump,Listen,Move Silently,Spot|5|PREDEFAULTMONSTER:Y`

**Update to RSRD**\
 The calculations for coming up with skill ranks is the same as in 3.0
so I will just present the revised tags. Note that you also need to
account for synergy bonuses when calculating ranks.\
 BONUS:SKILLRANK|Concentration,Escape Artist,Hide,Listen,Move
Silently,Search,Sense Motive,Spot|25|PREDEFAULTMONSTER:Y\
 BONUS:SKILLRANK|Diplomacy|23|PREDEFAULTMONSTER:Y\
 BONUS:SKILLRANK|Spellcraft|21|PREDEFAULTMONSTER:Y\
 For the Ninja Monkey the skill ranks would be divided as follows:\
 BONUS:SKILLRANK|Hide,Move Silently|4|PREDEFAULTMONSTER:Y\
 BONUS:SKILLRANK|Listen,Spot|3|PREDEFAULTMONSTER:Y\

------------------------------------------------------------------------

**`BONUS:SKILL`**

Several races get racial modifiers to certain skills.  Some of them are
listed in the race write up (often these are skills such as Search, Spot
and Listen), and some (movement related ones) are not.  (Gotta love
WotC). Creatures that have a natural Climb movement rate get a +8 to the
Climb skill.  Creatures that have a natural swimming movement rate get
+8 to their Swim skill.  These bonuses are now coded in the skill entry 
however so we do not need to enter them in the race file.

We apply these racial skill bonuses using the `BONUS:SKILL` tag.  You
can use this tag for a single skill, or multiple ones separated by
commas as long as the bonus value is the same for each skill.  If there
are two skills with two different bonus values, you have to use two
separate `BONUS:SKILL` tags.

To indicate that these are Racial bonuses we add " `|TYPE=Racial` " to
the end of the tags.

Reading through the Solar write-up we discover that they do not get any
racial bonuses to skills.

For the Ninja Monkey, I'm going to give them a +4 racial bonus to both
Balance and Jump checks.  Our tag for this would be:

> `BONUS:SKILL|Balance,Jump|4|TYPE=Racial`

**Update to RSRD**\
 The "hidden" bonuses referred to above are explicitly spelled out in
the RSRD.

------------------------------------------------------------------------

**`MFEAT`** ( <span class="new"> Deprecated </span> ) This tag is no
longer supported by PCGen.

**Note:** The PCGen data team is moving away from using the "Default
Monster" setting.  Default Monster Kits are being used instead.

To grant racial feats we use the `MFEAT` tag.  This is very similar to
the `MONCSKILL` tag in that the tag is followed by a list (of feats
instead of skills) separated by the pipe character.

To determine a race's feats we simply look in the "Feats" section of
their listing.

A couple of things to pay special attention to when entering feats using
the `MFEAT` tag:  Often a race will have a feat multiple times, but with
a different target, such as Weapon Focus with their claws and their
bite.  This would be entered as a single entry with two targets, like
this:  Weapon  Focus(Bite,Claw).

It should also be noted that there should be no space between the feat
name and the left paren.  This is true whenever you reference a feat
with a target, in any kind of .lst file.

Our entry using this tag for the Solar would be:

> `MFEAT:Cleave|Dodge|Great Cleave|Improved Initiative|Mobility|Power Attack`

**Update to RSRD**\
 The racial feats for a Solar in the RSRD are coded as follows:\
 MFEAT:Cleave|Dodge|Great Cleave|Improved Initiative|Improved
Sunder|Mobility|Power Attack|Track\
 No feats were listed in the original Ninja Monkey writeup so I selected
Alertness and Improved Initiative.  This would be coded as:\
 MFEAT:Alertness|Improved Initiative\

------------------------------------------------------------------------

`      CR     `

The CR tag is used to set the challenge rating for the race. It takes
the form of CR:&lt;number&gt;. A creature with a challenge rating of 4
would get a "CR:4" tag. One with a challenge rating of 1/2 would get
"CR:1/2".

The Solar has a challenge rating of 19, so the tag would read " `CR:19`
".

The Ninja Monkey has a challenge rating of 2, so his tag would read "
`CR:2` ".

**Update to RSRD**\
 The Solar's challenge rating in the RSRD is 23 so the tag would be
"CR:23".

------------------------------------------------------------------------

**`PREALIGN`**

Next up is our race's alignment.  In many cases while a certain race
might lean towards one alignment, they don't always have to be that
alignment.  The key word to look for when creating LST files and doing
alignments is "always".  Looking at the alignment entry for a Solar, we
see that is says "Always good (any)".  So we need to restrict the
alignments available to the race to the 'good' ones.

To set the alignment a creature MUST be, we use the PREALIGN tag.  The
format is "PREALIGN:\#,\#,\#" and the requirement is that the race be
one of the listed alignments.

The alignments have been defined by numbers as follows: 0 (Lawful Good),
1 (Lawful Neutral), 2 (Lawful Evil),  3 (Neutral Good), 4 (True
Neutral), 5 (Neutral Evil), 6 (Chaotic Good), 7 (Chaotic Neutral), 8
(Chaotic  Evil).

**Note:** In PCGen versions after 5.7.6 you can (and should) use the two
letter abbreviations for alignments: LG,LN,LE,NG,TN,NE,CG,CN,CE.

Since the Solars must be of good alignment, the tag for them will read "
`PREALIGN:0,3,6` ".

The Ninja Monkey race is usually Chaotic Good, but not always, so we
will simply not put in a PREALIGN tag for them.

------------------------------------------------------------------------

`      HITDICEADVANCEMENT     `

We use the HITDICEADVANCEMENT tag for those races that change size as
their hitdice change. It takes the format of
HITDICEADVANCEMENT:\#,\#,\#. The "\#" should be replaced by the number
corresponding to the last number of HD for that size. For a race that
was Small from 3-4 HD, Medium from 5-6 HD and Large from 7-10 HD the tag
would read "HITDICEADVANCEMENT:4,6,10".

When the race advances by class or has no advancement listed this tag
should be left out.

The solar shows an advance of 22-33 for Large size and 34-66 for Huge.
So the tag for him will be " `HITDICEADVANCEMENT:33,66` "

For the Ninja Monkey, he's advances by character class, so will get no
HITDICEADVANCEMENT tag.

------------------------------------------------------------------------

`      LEVELADJUSTMENT     `

The LEVELADJUSTMENT tag is used for those races that might conceivably
be used as player characters to keep them in balance with all the
regular PCs.

The Solar is such a high-level creature that it does not have a level
adjustment.

The Ninja Monkey, due to his several small special abilities would get a
+2 level adjustment, so his tag would read " `LEVELADJUSTMENT:2` ".

------------------------------------------------------------------------

**`FAVCLASS`**

We use the FAVLASS tag to set a race's favored class.  The Solar doesn't
have one, so we'll skip this tag for them, but I want the Ninja Monkey
favored class to be Monk.

On the Ninja Monkey line I put in a tab or two and then enter:

> `FAVCLASS:Monk`

------------------------------------------------------------------------

**`LANGAUTO`**

Many races get certain languages automatically by the simple virtue of
being of that race.  To grant these languages to the races we create we
use the LANGAUTO tag.  Immediately following the tag is a comma
delimited list of the languages the race receives.

Looking at the Solar listing, it says nothing about languages in the
specific description, but again in the general section about all
celestials, it says they speak Celestial, Infernal and Draconic.  So our
LANGAUTO tag for them will look like this:

> `LANGAUTO:Celestial,Infernal,Draconic`

For the Ninja Monkey I think the only two languages I'll grant them
automatically are their own Monkey  language and Common, so their tag
will look like this:

> `LANGAUTO:Common,Monkey`

------------------------------------------------------------------------

**`LANGBONUS`**

Races that can be player character races generally also have a number of
bonus languages that the creature can pick from when spending its
Int-based language picks.  The tag for this works just like the
`LANGAUTO` tag.

Since the Solar can't really be a player character no bonus languages
are listed so we skip this tag.

For the Ninja Monkey I will grant them Elven, Goblin, and Sylvan as
their bonus languages.

> `LANGBONUS:Elven,Goblin,Sylvan`

------------------------------------------------------------------------

**`LEGS`**

The LEGS tag is used to denote the number of legs a creature has. PCGen
uses this in the calculation of what the load/encumbrance ranges for a
race are. Sometimes the description of the race will tell you how many
legs it has, sometimes you have to just refer to the pictures provided.
:p

Both the Solar and our Ninja Monkey have two legs, so the tag for both
races will be " `LEGS:2` ".

------------------------------------------------------------------------

`      HANDS     `

The HANDS tag is used to denote the number of hands a creature has. This
is used to determine how many weapons it can hold. When you go to the
equipping screen it will offer to let you equip weapons to your primary
hand and and also show a location for each secondary hand. So a creature
with four hands could equip one weapon as primary and three as
secondary. This tag has no affect on a race's natural attacks.

The Solar and our Ninja Monkey both have two hands, so our tag for both
races would be " `HANDS:2` "

------------------------------------------------------------------------

`      SPELLS     `

The `SPELLS` tag is used to grant innate spellcasting (and some
spell-like abilities). We use it for spell-like abilities when they
grant the full spell effect. If it is restricted in some way (some races
can use a summon monster spell but only to summon a certain creature,
etc.), we simply list it as an SA.

Alternately, you can create a version of the spell with the
modifications the race needs included in the description.  The spell
should be added with no `CLASS` or `DOMAIN` tags.  Once the spell is
created you can use the `SPELLS` as normal.

The format is SPELLS:&lt;name of spellbook&gt;|TIMES=&lt;times per
day&gt;|CASTERLEVEL=&lt;level the spell is cast at&gt;|&lt;name of
spell&gt;,&lt;DC of spell&gt;|&lt;name of spell&gt;,&lt;DC of
spell&gt;|etc... If you put a "-1" in the times per day slot that means
that they can use the spell at will, and on output, "At Will" will
appear in the spell listing. For the spellbook name, we usually use
"Innate" for racial spells.

The Solar has a whole listing of spells, so the tag for them would be:

> `SPELLS:Innate|TIMES=-1|CASTERLEVEL=20|Aid|Animate Objects|Commune|Continual Flame|Dimensional Anchor|Greater Dispelling|Holy Smite,21|Imprisonment|Improved Invisibility (Self Only)|Lesser Restoration|Remove Curse|Remove Disease|Remove Fear|Resist Elements|Summon Monster VII|Speak with Dead            SPELLS:Innate|TIMES=3|CASTERLEVEL=20|Blade Barrier,23|Earthquake,25|Heal|Permanency|Resurrection|Shapechange,            SPELLS:Innate|TIMES=1|CASTERLEVEL=20|Greater Restoration|Mass Charm,25|Power Word (Blind),25|Power Word (Kill),26|Power Word (Stun),24|Prismatic Spray,24|Symbol,24|Wish`

The Ninja Monkey has one very simple spell-like ability and that is Pass
without Trace at will. The monster description does not specify a caster
level for the ability so we will leave that field blank.  The tag would
then look like:

> `SPELLS:Innate|TIMES=-1|Pass Without Trace`

------------------------------------------------------------------------

`      SOURCEPAGE     `

This is just what it seems, where we indicate the page from the source
material where you can find the text and stats for the race.

When you are going from an OGL book the format is usually
SOURCEPAGE:p.\#

If you are working from an online document such as the SRD, it would be
the filename, so SOURCEPAGE:&lt;filename&gt;/

For the solar, we pulled him from the SRD so his tag would be "
`SOURCEPAGE:srdmonstersc.rtf` ".

The Ninja Money is from my custom races file, so Il make the tag for him
" `SOURCEPAGE:customraces.txt` ".

------------------------------------------------------------------------

Well, this brings to a close the lessons on creating monster races for
use in PCGen. Hopefully everything I've talked about has made sense to
you all. :)

Barak\
 LST Chimp



