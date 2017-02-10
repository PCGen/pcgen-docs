+++
date = "2016-08-01"
title = "Lesson #4: .lst - Races (part 2)"
original_url = "/list/lst-file-class/04-race-2.html"

[menu.main]
    identifier = "lst-file-class_04-race-2"
    name = "Lesson #4: .lst - Races"
    parent = "lst-file-class"
    
+++
By Professor Chris Chandler (Barak).

**File(s) Covered:** \*races.lst

**Tags used:**

`      BONUS:COMBAT|AC          ,           BONUS:COMBAT|BAB          ,           NATURALATTACKS          ,           FACE          ,           REACH          ,           AUTO:EQUIP          ,           AUTO:ARMORPROF          ,           AUTO:WEAPONPROF     `

Not much to say before we jump into things this time. This is a
continuation from lesson \#3 in our look at creating race files.

------------------------------------------------------------------------

**`BONUS:COMBAT|AC`**

Up next on our list to do is the race's armor class. In this section
we'll deal with special bonuses that affect a races AC value. We won't
worry about the effects of Dexterity and size adjustments because those
are handled automatically by PCGen once we code in their dexterity score
and size.

The first and most common of these is a race's natural armor. In the SRD
listings it can be found in parentheses after the total AC for the race.
Looking at the entry for the Solar: "AC:35 (-1 size, +5 Dex, +21
natural)".

We would enter the bonus from natural armor for the Solar using the
following tag " `BONUS:COMBAT|AC|21|TYPE=NaturalArmor.REPLACE` ". Quite
the tag, eh? :P

To break it down a bit further, " `BONUS:COMBAT|AC` " directs PCGen to
apply the bonus to the character's/monster's AC. "21" is the value of
the bonus to be applied of course. The " `TYPE=whatever` " sets the type
of bonus for stacking purposes. It should be noted that "
`TYPE=NaturalArmor` " is a special type in that it causes the program to
separate those bonuses out from other AC bonuses when sent to the output
sheet.

The ".REPLACE" is used to make sure that stacking with items and other
things that affect natural armor, such as an amulet of Natural Armor, is
allowed.

I think a bit of a digression is in order to explain how PCGen handles
stacking issues.

1\) If a bonus does not have a type associated with it, the program
assumes it will stack with anything.

> Example:\
>  " `BONUS:COMBAT|AC|2` " and " `BONUS:COMBAT|AC|1` " will stack for a
> total bonus to the AC of +3.

2\) If a bonus does have a type, it will stack with all different types,
but not it's own type. When there are two bonuses with the same type
(and no suffixes that modify this rule) the program will choose and
apply the largest of them.

> Examples:\
>  a) " `BONUS:COMBAT|AC|2|TYPE=NaturalArmor` "\
>  and " `BONUS:COMBAT|AC|1|TYPE=Deflection` "\
>  will stack for a total bonus to the AC of +3.
>
> b\) " `BONUS:COMBAT|AC|2|TYPE=NaturalArmor` "\
>  and " `BONUS:COMBAT|AC|1|TYPE=NaturalArmor` "\
>  will not stack and there will be a total bonus to the AC of +2.
>
> c\) " `BONUS:COMBAT|AC|2|TYPE=NaturalArmor` "\
>  and " `BONUS:COMBAT|AC|1|TYPE=NaturalArmor` "\
>  and " `BONUS:COMBAT|AC|1|TYPE=Deflection` "\
>  will give you a total bonus to ac of +3.

3\) When you use the " `.REPLACE` " suffix, the program takes all like
bonuses that have " `.REPLACE` " appended and adds them together, and
THEN compares that result to all other like bonuses to determine which
to use.

> Examples:\
>  a) " `BONUS:COMBAT|AC|2|TYPE=NaturalArmor.REPLACE` "\
>  and " `BONUS:COMBAT|AC|1|TYPE=NaturalArmor.REPLACE` "\
>  will stack and there will be a total bonus to the AC of +3.
>
> b\) " `BONUS:COMBAT|AC|2|TYPE=NaturalArmor.REPLACE` "\
>  and " `BONUS:COMBAT|AC|2|TYPE=NaturalArmor.REPLACE` "\
>  and" `BONUS:COMBAT|AC|1|TYPE=NaturalArmor` "\
>  will give you a total bonus to ac of +4.

For further examples [see the BONUS page of the
documentation](/list/global/bonus.html) .

Back to creating our race file...

For the Ninja Monkey, we'll give them a natural armor of 2 for having a
thick pelt. The tag for that would be:

> `BONUS:COMBAT|AC|2|TYPE=NaturalArmor.REPLACE`

At this time we should also cover any other special AC enhancements the
race might have. Looking through the SRD write-up on the Solar, there is
nothing else for them, so we're done there.

For the Ninja Monkey however, I'm going to give a +2 divine bonus to
their AC since they are the creation and favored race of a minor godlet
in my world, and he tries to protect them. The tag for this would be:

> `BONUS:COMBAT|AC|2|TYPE=Divine` ".

------------------------------------------------------------------------

**`BONUS:COMBAT|BAB`**

**Note:** The PCGen data team is moving away from using the "Default
Monster" setting.  Default Monster Kits are being used instead.

Next comes one of the most important bits, but also one of the most
involved. We need to set the BAB (Base Attack Bonus) of the race. What
makes this so involved (at least when coding in other peoples creations)
is that the BAB is not listed. You have to look at the attack bonuses
given (in the attack line in the SRD) and then work backwards from
there, taking out any bonuses for size, stat (strength or dex), epic
bonuses, and any feats that might affect it.

Looking to the Solar once again, we see the following listed for it's
attacks: "Attacks: +5 dancing vorpal greatsword +35/+30... melee"

So, this tells us we start with a final value of 35. From that we need
to subtract 5 (for the magic weapon), 9 (for his 28 strength), 1 (for
his size). Then we add 1 since at 22 hit dice he is considered epic and
gets a +1 epic bonus. The race has no feats that affect BAB, so our BAB
total is 35-5-9-1+1=21.

These values are only used when you are creating a "default monster" so
we will append the `PREDEFAULTMONSTER:Y` tag to the bonus. This
basically tells the program not to apply the bonus unless the user has
selected "Use Default Monsters" in the preferences tab. This BAB bonus
is also the base for the race and needs to stack with feats and other
things that actually modify the base BAB, so we'll give it a "
`TYPE=Base.REPLACE` ". Our tag will look like this:

> `BONUS:COMBAT|BAB|21|PREDEFAULTMONSTER:Y|TYPE=Base.REPLACE`

The Ninja Monkey (since we are creating this race on the fly) we can
just pick a number for. I'll just give him a +5. I may come back later
and revise this if it's too much after I add all the other stuff. The
tag for this will be:

> `BONUS:COMBAT|BAB|5|PREDEFAULTMONSTER:Y|TYPE=Base.REPLACE`

**Update to RSRD**\
 The BAB is explicited listed under the Base Attack heading in 3.5 so no
calculation is needed.

------------------------------------------------------------------------

`      NATURALATTACKS     `

The NATURALATTACKS tag is what we use to define non-equipment attacks a
race may possess. This tag does several things at once. It creates a
piece of "equipment" that will show up in the GUI to be equipped (which
it is by default). It creates and grants a weapon proficiency for the
defined natural attack to make sure the creature doesn't receive the
standard -4 non-proficiency penalty. It determines what kinds of damage,
how much damage, what kind of attack (melee or ranged), how many attacks
with the defined natural attack and whether or not that attack gets
iterative attacks or not.

The first attack listed after the tag is considered to be the primary
attack, and all others are treated as a secondary attack (at -5 unless
some feat modifies that).

The format for the tag is as follows: NATURALATTACKS:&lt;attack
name&gt;,&lt;TYPE line&gt;,&lt;\*(if
non-iterative)&gt;&lt;\#attacks&gt;,&lt;damage&gt;

The &lt;attack name&gt; is what you want to appear as the name for the
natural attack. This can be things like Bite, CLaw, Tentacle Rake or
Incorporeal Touch just to name a few common examples.

The &lt;TYPE line&gt; is similar to the TYPE line we use in .lst files
for regular weapons. The line must start with "Weapon.Natural". It is
then followed by the type of attack ("Ranged" or "Melee") and then any
descriptors for the type of damage it deals ("Piercing" and "Slashing"
and "Bludgeoning" are good examples of this). You do not have to use
just one, you could (and often do) have things like "Piercing.Slashing".

Next would come the number of attacks. If it says something like "two
claws +21" then they only get that many attacks and they are not
iterative, so we put a "\*" in front of the number. If it says something
like "Slam +15/+10/+5" then they do get iterative attacks and the
asterisk is left out (these are few and far between, but they do exist).

Finally we list the damage the attack does (dice damage only, STR
modifiers and other adjustments will be applied by PCGen). This is
entered in the standard dice notation such as "1d8" and "4d10".

The Solar has no natural attacks, so we'll skip this tag for them.

The ninja monkey has claws (2) which do 1d4 points of damage for it's
primary natural attack and a bite which does 1d8 for its secondary
attack. The tag for the ninja monkey would look thus:

> `NATURALATTACKS:Claw,Weapon.Natural.Melee.Piercing.Slashing,*2,1d4|Bite,Weapon.Natural.Melee.Piercing.Slashing.Bludgeoning,*1,1d8`

Note that with creative manipulation within the PCGen Gui, you can make
it so that an attack listed as secondary shows with primary attack
numbers which is sometimes necessary to make the numbers come out
properly. (Basically, once you equip it, right click on it and change
the location to "Carried").

------------------------------------------------------------------------

**`FACE`**

Each creature has a face that represents the amount of space the
creature takes up on the battlegrid.  The face setting is represented by
two numbers width and length. This setting is not used in any way by the
PCGen program and is simply used to output the correct value on the
character sheet.

We use the `FACE` tag to define this characteristic.  The format is "
`FACE:width,length` ".

Both the Solar and the Ninja Monkey have a face of 5 ft. by 5 ft. so we
will enter " `FACE:5,5` " to both entries.

Some creatures have fractional face settings like 2 1/2 ft. PCGen needs
the decimal representation for these numbers so you would need to enter
2.5 for 2 1/2.

**Update to RSRD**\
 In the revised rules, face is called Space and is represented by a
single number. We continue to use the `FACE` tag and enter just the one
number.

------------------------------------------------------------------------

**`REACH`**

Every creature has a reach.  This is usually defined by the size of the
character, but certain creatures (like  those with long tentacles) have
a longer reach than they normally would for a creature of their size.

We use the REACH tag to define this characteristic.  The format is
"REACH:distance".

A Solar has a reach of 10 feet since it is a large creature, so on it's
line we'll enter " `REACH:10` ".  The  Ninja Monkey is a medium size
creature (w/o tentacles  :p) so it will get the standard reach for a
medium-size creature of 5 feet.  " `REACH:5` " goes on his line.

------------------------------------------------------------------------

AUTO:EQUIP

**Note:** The PCGen data team is moving away from using the "Default
Monster" setting.  Default Monster Kits are being used instead.

When a racial entry lists weapons (other than natural) or armor the race
is considered to come with the mentioned equipment.  To grant equipment
automatically we use the `AUTO:EQUIP` tag.  Despite it's name, it
doesn't actually equip the gear, it only puts in in the "owned gear"
list (for lack of a better term).  The user creating the creature will
have to go to the gear tab and actually equip it.

Note that you cannot use a name with a mathematical symbol in it (such
as "+5 Vorpal Greatsword").  You can get around this by creating a
different name for a piece of equipment ("Solar Greatsword") and using
`OUTPUTNAME` in the equipment .lst ( `OUTPUTNAME:+5 Vorpal Greatsword`
).  We'll cover this in more detail when we go over equipment.

Examining the Solar entry, we see that they have the aforementioned +5
Vorpal Greatsword as well as a +2 mighty longbow.  I'll create special
equipment.lst files for these, and use the names "Solar Longsword" and
"Solar Longbow".

The tag granting these pieces of equipment to the Solar would thus be "
`AUTO:EQUIP|Solar Greatsword|Solar  Longbow` ".

For the Ninja Monkey I think I'll give him Leather armor and a regular
dagger.  The tag for this would be  " `AUTO:EQUIP|Leather|Dagger` ".

------------------------------------------------------------------------

**`AUTO:ARMORPROF`**

When a racial entry lists an armor for a race, the race is proficient
with the type of armor in that class and all lesser types.  So if an
entry is shown for a Medium type armor, the race would be proficient
with Medium \*and\* light armors.  To grant these proficiencies, we use
the `AUTO:ARMORPROF` tag.  This tag is the same in format as the
`AUTO:EQUIP` tag.  It will take armors by name and grant only
proficiency with that type, or by `TYPE` and grant proficiency to every
type of armor in that selection.

Looking at the Solar entry, there is no armor listed, so we'll skip this
tag for them.

The Ninja Monkey has Leather armor (which is Light) so we'll put in a
tag of " `AUTO:ARMORPROF|TYPE=Light` " for them.

------------------------------------------------------------------------

`      AUTO:WEAPONPROF     `

When a race has a weapon (or weapons) other than natural ones listed
they are considered to be proficient with them.  To grant these weapon
proficiencies, we use the `AUTO:WEAPONPROF` tag.  It has the same format
as the last two tags we covered.  Note that you need to put the
appropriate proficiency name in this tag, NOT the weapon name.

Since the Solar uses a greatsword and a composite longbow, the entry for
them is  " `AUTO:WEAPONPROF|Greatsword|Longbow (Composite)` ".

The Ninja Monkey only has a dagger, so the entry for him will be "
`AUTO:WEAPONPROF|Dagger` ".

**Update to RSRD**\
 In the RSRD Composite bows use the proficiency for the non-composite
version so the Solar tag would be:\
 AUTO:WEAPONPROF|Greatsword|Longbow

------------------------------------------------------------------------

And we'll call it a day at this point. I know that's only a few more
tags, but there's a lot to digest in those tags and I'm sure there will
be questions so I'm going to call that the end of this lesson.

I would heartily recommend looking up these tags in the docs to discover
all of the ways in which they can be used.

Barak\
 LST Chimp



