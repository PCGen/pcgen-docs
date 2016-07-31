+++
date = "2016-08-01"
title = "Lesson #3: .lst - Races (Part 1)"
original_url = "/list/lst-file-class/03-race-1.html"

[menu.main]
    identifier = "lst-file-class_03-race-1"
    name = "Lesson #3: .lst - Races (Part 1)"
    parent = "lst-file-class"
    
+++
By Professor Chris Chandler (Barak).\
 Updated by Aaron Divinsky (boomer70).

**File(s) Covered:** \*races.lst

**Tags used:**

`      OUTPUTNAME          ,           SIZE          ,           RACETYPE          ,           RACESUBTYPE          ,       TYPE (TYPE is deprecated: Replaced by RACETYPE and RACESUBTYPE)      ,           MONSTERCLASS          ,           HITDICE          ,           MOVE     `

------------------------------------------------------------------------

This is the beginning of several lessons that will be necessary to cover
the creation of a race file. There are many tags, and some of them will
take some seriously long explanations, so get some munchies and a drink,
get comfortable and we'll get started.

Since the race lines can get exceedingly long, and yahoo will wrap my
lessons, I'll also post a file that may be perused as you're reading
this. (Be sure to turn off word-wrap on your text file reader!)

I'm going to develop a file that contains two races. One will be from
the System Reference Document (SRD) so you can see how  to do an already
existing race and the other I'm going to make up on the fly and use to
demonstrate every tag I can remember. :p

One thing to note is that these will be considered "monster" races.
Towards the end of the lesson i'll go back through and create a player
character only race.

We'll do a Solar and, ummm, I know! Ninja Monkeys! :) The lessons will
follow the format of a standard monster write up. A sample monster write
up for our Ninja Monkey race is presented below so you can follow along
(in RSRD format)

------------------------------------------------------------------------

**Ninja Monkey**

Medium Monstrous Humanoid

**Hit Dice:**

4d8+8 (26 hp)

**Initiative:**

+8

**Speed:**

30 ft. (6 squares), climb 20 ft.

**Armor Class:**

20 (+4 Dex, +2 Natural, +2 Divine, +2 Leather armor), touch 14,
flat-footed 16

**Base Attack/Grapple:**

+4/+7

**Attack:**

Claw +7 melee (1d4+3) or dagger +7 melee (1d4+3)

**Full Attack:**

2 claws +7 melee (1d4+3) and bite +2 melee (1d8+1) or dagger +7 melee
(1d4+3)

**Space/Reach:**

5 ft./5 ft.

**Special Attacks:**

—

**Special Qualities:**

Darkvision (60'), DR 3/-, immunity to poison

**Saves:**

Fort +3, Ref +8, Will +6

**Abilities:**

Str 17, Dex 18, Con 14, Int 11, Wis 15, Cha 10

**Skills:**

Balance +8, Hide +8, Jump +7, Listen +7, Move Silently +8, Spot +7

**Feats:**

Alertness, Improved Initiative

**Environment:**

Forests

**Organization:**

Solitary or Gang (2-4)

**Challenge Rating:**

2

**Treasure:**

Standard (double bananas)

**Alignment:**

Usually Chaotic Good

**Advancement:**

By character class

**Level Adjustment:**

+2

Skills: Ninja monkeys have a +4 racial bonus to Balance and Jump checks.
Ninja monkeys have a +2 racial bonus in forested environments.

<span class="s18"> Ninja Monkey Characters </span>\
 — Automatic Languages: Common and Monkey, Bonus Languages: Elven,
Goblin, Sylvan.\
 — Favored Class: Monk

------------------------------------------------------------------------

First, a couple of general rules:  Every tag needs to be separated with
tabs. Spaces may be used within names, etc, but never at the beginning
or end. There should never be a space-tab or a tab-space combination as
this will make the parser choke and die.

Although any text editor will do, a text editor that can do syntax
colorization is also a good idea. I use a program called TextPad. You
can also use UltraEdit and I believe there is one called Crimson. You
can find a number of these syntax files on the Yahoo! Group
[PCGen\_experimental](http://groups.yahoo.com/group/pcgen_experimental)
.

I'll use "mystuff\_races.lst" as the file name. This conforms to the new
naming convention adopted by the PCGen lstmonkey crew recently.
Basically it is in the format of "source\_filetype.lst".

**Update to RSRD**\
 These classes were originally written using the SRD (3.0 rules).
Throughout you will find sidebars like this one with notes on the
differences between the 3.0 rule set and the 3.5 rule set as found in
the Revised System Reference Document (RSRD).

------------------------------------------------------------------------

Race Name

The race file is currently a lst file that has one racial entry per
line. The first thing on each line is the race name. There is no tag for
it, the program assumes that whatever is there is the name of a race.

One thing to consider when entering the race name is grouping (all
demons together, etc). A Solar is a celestial, and we'd like it to show
up with other celestials, so the name I'm going to enter will be
"Celestial (Solar)". On the next Line I'll enter "Ninja Monkey".

**Update to RSRD**\
 In the RSRD the Solar is listed as an Angel not a Celestial. Therefore
we would name it "Angel (Solar)".

------------------------------------------------------------------------

**`OUTPUTNAME`**

Now, "Celestial (Solar)", while making it easy to find in the race list
with the other celestials will look kind of funny on output, so we'll
use the OUTPUTNAME tag to change what will appear on output (if the user
has the preference checked to use it).

The OUTPUTNAME tag can be used in a couple of different manners. You can
completely change the name of an object (as far as output is concerned)
and not reference the real name at all, or you can use part of the real
name. A special string was developed to grant access to only the text
contained in parentheses. That string is "\[NAME\]" (no quotes).

So, if we wanted the name on output to be "Celestial, Solar", we could
do it two different ways. 1) OUTPUTNAME:Celestial, Solar or 2)
OUTPUTNAME:Celestial, \[NAME\].  I don't like either one of those... I
just want it to be called a "Solar" on output, so I'm entering the tag
like this:

> `OUTPUTNAME:[NAME]`

The name "Ninja Monkey" is just fine as it is, so we'll skip an
OUTPUTNAME tag on this one.

------------------------------------------------------------------------

`      SIZE     `

Every creature has a size.  The size tag uses the first letter of each
size category, so the possible choices are F (Fine), D (Diminutive), T
(Tiny), S (Small), M (Medium), L (Large), H (Huge), G (Gargantuan), and
C (Colossal).

The Solar is a Large creature so on that line we'll enter a couple tabs
and then put " `SIZE:L` ". The Ninja Monkey is man-sized (Medium), so
we'll put " `SIZE:M` " on that line.

------------------------------------------------------------------------

`      RACETYPE/RACESUBTYPE     `

After the creature's size the next information is the race type. For the
Solar it is listed as Outsider (Good). The information in the brackets
after the type lists all the subtypes for the monster, in this case
Good. We will enter " `RACETYPE:Outsider` " put in a tab and enter "
`RACESUBTYPE:Good` ".

For the Ninja Monkey we have to enter just the type with no subtypes.

> `RACETYPE:Monstrous Humanoid`

**Update to RSRD**\
 The Solar changes subtypes in the RSRD to Outsider (Angel, Extraplanar,
Good). Therefore we need to change our subtype entry to read
`RACESUBTYPE:Angel|Extraplanar|Good` .

------------------------------------------------------------------------

`      TYPE     `

**Note:** This use of TYPE has been deprecated and is replaced with
`RACETYPE/RACESUBTYPE` .

We use the TYPE tag to indicate what type of creature the race is
(Aberration, Undead, Animal, Monstrous Humanoid, Magical Beast, etc.).

The Solar is an Outsider so our tag would read " `TYPE:Outsider` ".

The Ninja monkey is a Monstrous Humanoid so our tag would be "
`TYPE:Monstrous Humanoid` ".

------------------------------------------------------------------------

`      MONSTERCLASS     `

The MONSTERCLASS tag is used by the program when the "Default Monster"
setting is off. It tells it how many and which monster class levels to
give the race (as opposed to using the HITDICE tag when in "Default
Monster" mode).

The tag takes the format of
MONSTERCLASS:&lt;monsterclassname&gt;:&lt;levels&gt;. For PCGen
distribution files the class name is \*usually\* the type of creature
and the number of levels is usually set equal to the number of HD the
default creature has. An exception to this is when the racial
description says they are spellcasters... "cast as 18th level
sorcerers". In that case we create a special class (in a class.lst file)
to grant the race the appropriate spellcasting levels.

The Solar is an Outsider with 22 HD, and he casts spells as a 20th level
cleric, so his tag would be " `MONSTERCLASS:Solar:22` "

For the Ninja Monkey, he's a Monstrous Humanoid and has 4 HD and no
spellcasting ability, so the tag for him would read "
`MONSTERCLASS:Monstrous Humanoid:4` ".

------------------------------------------------------------------------

`      HITDICE     `

**Note:** The PCGen data team is moving away from using the "Default
Monster" setting. Default Monster Kits are being used instead.

This is the tag we use to indicate the die size and quantity of hit dice
a race gets. The program uses this when the "Default Monster" setting in
the preferences is on. It takes the format of
HITDICE:&lt;quantity&gt;,&lt;size&gt;. This information is found at the
top of each race listing.

The Solar has 22d8 hit points, so would have " `HITDICE:22,8` " for this
tag.

The ninja monkey has 4d8 hit points, so would have " `HITDICE:4,8` " for
this tag.

------------------------------------------------------------------------

**`MOVE`**

To define a race's movement modes and rates we use the MOVE tag. The
format is "MOVE:mode,rate,mode,rate".   You can enter as many movement
modes and rates as you want.

Looking at the Solar in the SRD, they list "SPEED:50ft,fly 150ft". The
first number is always their "Walk" (otherwise known as "Base") movement
rate, except for those races that can't walk like some plants. So on the
Solar's line we will enter (remember to put a tab or two between the
last tag and this new one):

> `MOVE:Walk,50,Fly,150`

I'm going to give the Ninja Monkey a walk rate of 30 and a climb rate of
20, so the tag for his line would be:

> `MOVE:Walk,30,Climb,20`

------------------------------------------------------------------------

I'm going to end this lesson at this point. If you have questions,
please post them to the Yahoo! group
[PCGenListFileHelp](http://groups.yahoo.com/group/PCGenListFileHelp) .

The example file for this lesson can be found at the [LSTfileclass Yahoo
Group](http://games.groups.yahoo.com/group/LSTfileclass/) in the files
section
[here](http://f2.grp.yahoofs.com/v1/EKxcQRSQkNqrtFjDTDyZ5ZvY6XxwOMY5DToAK4c8KwnppEP1vNZ7czz_HnUk-%20vVPAEAIj4d1fL_uy8smyJGnXeTZ1TeVuQ/Lesson%20Files/mystuff_races.lst)
.

Barak\
 LST Chimp



