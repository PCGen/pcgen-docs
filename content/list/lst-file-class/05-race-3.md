+++
date = "2016-08-01"
title = "Lesson #5: .lst - Races (part 3)"
original_url = "/list/lst-file-class/05-race-3.html"

[menu.main]
    identifier = "lst-file-class_05-race-3"
    name = "Lesson #5: .lst - Races (part 3)"
    parent = "lst-file-class"
    
+++
By Professor Chris Chandler (Barak).

**File(s) Covered:** \*races.lst

**Tags used:**

`      SA          ,           FEAT          ,           VFEAT          ,           VISION          ,           SR          ,           DR          ,           TEMPLATE          ,           BONUS:CHECKS          ,           BONUS:STAT     `

------------------------------------------------------------------------

This lesson will cover Special Attack and Special Qualities and all the
tags that are involved in putting them into PCGen.  As with most things
in PCGen there are a number of different ways to accomplish the same
thing.  We will try and cover the preferred methods and simply note that
there maybe other ways to do what you want. As always, you should check
the documentation for more information.

------------------------------------------------------------------------

`      SA     `

This is the tag we use for any special abilities, attacks or qualities
the race may have. Things that would be noted here are immunities,
bonuses to skills that are conditional ("+8 to spot in daylight" is a
good example of this type) and other things of that kind. If the type of
special ability/quality is listed it should be added in parens. "(Ex)"
for extraordinary, "(Sp)" for Spell or Spell-like, "(Su)" for
supernatural. We wouldn't list anything that has a tag like Spell
Resistance or Damage Reduction or spells.

The Solar has several abilities such a Aura of Menace, Protective Aura,
etc. (essentially his celestial qualities) that we should list. So his
set of SA\
 tags (separated by tabs of course) would look like:

> `SA:Aura of Menace (Su)            SA:Magic Circle against Evil (Su)            SA:Protective Aura (Su)            SA:Teleport (Su)            SA:Tongues (Su)            SA:Immunity to electricity/petrification/cold/acid (Ex)            SA:Fire resistance 20 (Ex)            SA:Keen Vision (Ex)`

The Ninja Monkey is a hardy race so I'll give him immunity to poison.
Being a monkey, I'll also give him +2 to Hide in forested areas. So we
would put:

> `SA:Posion Immunity (Ex)            SA:+2 to Hide in forested areas`

**Update to RSRD**\
 The Solar's special abilities have changed a little in 3.5. His tags
would look like:\
`SA:Spell-Like Abilities          SA:Immunity to petrification/cold/acid (Ex)          SA:Protective Aura (Su)          SA:Regeneration % (Ex)|Regeneration          SA:Resistance to Fire 10 (Ex)          SA:Resistance to Electricity 10 (Ex)          SA:Tongues (Su)     `

------------------------------------------------------------------------

**`FEAT`**

At times a creature's special abilities have additional behavior we
would like to encode into the program.  A good example of this would be
a creature that gets an ability that is the same as a class feature,
like Sneak Attack or Rage.  These abilities are already in PCGen in what
is called a "Hidden Feat".  They can be found in the file
xsrd\_feats\_hidden.lst.  Basically they are exactly like normal feats
except they are not visible in the GUI so you can't select them as a
feat choice for your character.  We use the " `FEAT` " to grant these
abilities to a monster. It should be noted that only a single " `FEAT` "
tag can be present in a race line so if multiple feats need to be
granted they should be separated with a "|" (pipe) character.

Suppose we had a variation of our Ninja Monkey race that received the
Rage special ability as a Barbarian equal to their HD. We could code
this like so:

> `FEAT:Rage<tab>BONUS:VAR|RageTimesLvl,RagePowerLvl|HD`

------------------------------------------------------------------------

**`VFEAT`**

Similar to the `FEAT` tag, the `VFEAT` is used to grant feats to a
creature.  It is generally used to grant bonus feats particularly ones
that a creature may not ordinarily qualify for.  In the creature
description in the SRD, the feat will be noted as a bonus feat.

Neither the Solar nor our Ninja Monkey have any bonus feats so we won't
enter anything for either for this tag.

Just to illustrate if we look at the Marilith in the SRD, it is noted as
having both the Multidexterity and Multiweapon Fighting feats as bonus
feats.  We would therefore enter:

> `VFEAT:Multidexterity<tab>VFEAT:Multiweapon Fighting`

**Update to RSRD**\
 In the RSRD, bonus feats are indicated with a superscript "B" after the
feat name in the creature's list of feats.\
 The Marilith does not get the Mutlidexterity and Mutliweapon Fighting
feats as bonus feats in 3.5.

------------------------------------------------------------------------

**`VISION`**

We use the VISION tag to define the various types of vision a creature
has.  You can have more than one type of vision listed by using "|"
(pipe) character to separate them.  That makes the tag format
"VISION:type  (distance)|type (distance)".  Note that the (distance)
part is optional.

A creature's vision is (in most cases) defined by the type of creature
it is, unless it's description states otherwise.  In the case of the
Solar, it has no information on it's vision in it's description, but
there is  information in the section about ALL Celestials, so we'll use
that information. It says that all Celestials  have Darkvision with a
range of 60 feet and Low-light vision.  The tag for the vision of a
Solar would be:

> `VISION:Darkvision (60')|Low-light`

The Ninja Monkey I'm going to classify as a Monstrous Humanoid.
According to the section on Monstrous  Humanoids in the SRD
(srdcreatureoverview.rtf), Monstrous Humanoids get Darkvision with a
range of 60 feet.  Their tag will read:

> `VISION:Darkvision (60')`

------------------------------------------------------------------------

`      SR     `

For races that have Spell Resistance, we use the SR tag. This can take a
plain number or a formula for those races that get better SR with more
levels. So SR:12 is valid as is SR:11+TL.

The Solar has a spell resistance of 32, so we would enter " `SR:32` "
for him.

The Ninja Monkey has no SR so we'll skip this tag for them.

------------------------------------------------------------------------

`      DR     `

To indicate Damage Reduction for races we use the DR tag. It takes the
format of DR:&lt;reduction&gt;|&lt;bonus to bypass&gt;. So a creature
with a damage reduction of 5 unless you have a +1 weapon would be
"DR:5/+1". For a creature that has damage reduction of 10 unless it's a
silver weapon you would use "DR:10/Silver". If the race gets the damage
reduction regardless of what kind of weapon is used (such as a high
level barbarian gets) you use a "-" in the second position.

The Solar has a damage reduction of 35 and only a +4 or better weapon
can get through it, so the tag would read " `DR:35/+4` ".

The Ninja Monkey has a very strong connection with the earth and gains a
small damage reduction of 3 with no special weapons that can ignore it,
so the tag would be " `DR:3/-` ".

**Update to RSRD**\
 In the RSRD the Solar has a damage reduction of 15/epic and evil so we
would instead enter:\
`DR:15/epic and evil`\
 The Ninja Monkey's DR remains unchanged.

------------------------------------------------------------------------

`      TEMPLATE     `

We use templates (and the "TEMPLATE" tag) to apply all the bonuses that
creatures get from being a certain type of creature (ie: no CON score
for undead, etc.). The standard PCGen distribution has templates created
for all the creature types that are called out in the R/SRD.

The format is TEMPLATE:&lt;templatename&gt;. Despite what the
documentation says currently, you cannot apply multiple templates by
using a "|" to separate them, you must use a separate TEMPLATE tag for
each template you wish to apply.

The Solar is an outsider so we would add a " `TEMPLATE:Outsider` " to
his listing.

The Ninja Monkey is a Monstrous Humanoid and would get "
`TEMPLATE:Monstrous Humanoid` ".

**Note:** It is no longer necessary to add a template just for the
monster's type as it is handled by the monster's class. Some templates
are still required, like "Mindless" for creatures without and Int score
or "Incorporeal" for creatures without a corporeal form.

------------------------------------------------------------------------

**`BONUS:CHECKS`**

**Note:** The PCGen data team is moving away from using the "Default
Monster" setting.  Default Monster Kits are being used instead.

Now we are going to deal with coding in the race's bonuses to saving
throws.

For this part, like the Base Attack Bonus, we have to do a little
back-figuring. We find the final values in the race listing. For the
Solar it is "Saves: Fort +18, ref +18, Will +20". From these final
numbers we need to subtract the appropriate stat bonus (CON for
Fortitude, DEX for Reflex, and WIS for Willpower), feat bonuses, and
epic bonuses.

The Solar's Fortitude Save bonus will be 18 (final)-5 (CON mod)-1 (epic
bonus)=12. His Reflex Save bonus would be 18 (final)-5 (DEX mod)-1 (epic
bonus)=12. The Willpower Save bonus would be 20 (final)-7 (WIS mod)-1
(epic bonus)=12.

The tag we use to enter these values is `BONUS:CHECKS` . This tag has
two forms. The first is " `BONUS:CHECKS|checkname|#` " which would add
"\#" as bonus that would appear in the "Misc" box on the output sheet.
The second form (and the one we will use in our race files almost
always) is " `BONUS:CHECKS|BASE.checkname|#` ", which adds to the base
bonus and makes it appear in the "Base Save" column on the output
sheets. If the bonus is the same for multiple checks, you can do them in
one tag by separating them with a comma like this "
`BONUS:CHECKS|BASE.checkname1,BASE.checkname2|#` ".

Our good luck is that all of the Solar's bonuses are the same so we can
use one tag instead of three. Like the BAB, these values are only to be
used for default monsters, so we'll use the " `PREDEFAULTMONSTER:Y` "
suffix with it. The tag for the Solar would thus be:

> `BONUS:CHECKS|BASE.Fortitude,BASE.Reflex,BASE.Willpower|12|PREDEFAULTMONSTER:Y`

For the Ninja Monkey, my concept of him is that he's really quick and
agile, so we'll give him a +5 for his reflex saves, and a +2 to
Fortitude and Willpower. Since the bonuses are different we need to use
two tags. The tags would be:

> `BONUS:CHECKS|BASE.Reflex|5|PREDEFAULTMONSTER:Y`\
> `BONUS:CHECKS|BASE.Fortitude,BASE.Willpower|2|PREDEFAULTMONSTER:Y`

**Update to RSRD**\
 The Ninja Monkey would have Good Reflex and Will saves as a Monstrous
Humanoid. Therefore in the RSRD it would have base saves of Fort +1, Ref
+4, Will +4. In LST code this would be:\
`BONUS:CHECKS|BASE.Fortitude|1|PREDEFAULTMONSTER:Y`\
`BONUS:CHECKS|BASE.Reflex,BASE.Willpower|4|PREDEFAULTMONSTER:Y`

------------------------------------------------------------------------

**`BONUS:STAT`**

Now we come to the ability scores for the race.

This is complicated a bit by certain rules WotC has implemented.  If a
race is used as a character the odd scores need to be dropped  by one to
become even, while the "default monster" should have the additional 1 to
the stat.

Our first assumption when doing ability scores for races is that they
will be built on a starting ability  score of 10 in each stat. So we
need to subtract 10 from each score right off that bat.  Then, if the
ability  score is odd, subtract one more to make it even.  (For the
Solar these values would be STR 18, DEX 10, CON 10,  INT 12, WIS 14, CHA
14 with INT, WIS and CHA being odd). Now that we have the non-monster
values, we can put  them into the `BONUS:STAT` tag.

To designate which stat gets the bonus we use the abbreviations.  So for
strength it would be `BONUS:STAT|STR|#` .   Like the `BONUS:SKILL` tag,
you can apply the same bonus to more than one stat at once by making a
comma separated list such as `BONUS:STAT|STR,CON|#` .  One last note, if
the final stat value is 10 then there is no  need to add a bonus tag for
it.

Finally, to take care of the extra 1 stat point for certain stats for
default monsters we add one more tag,  lumping together all the stats
that were odd and adding a " `PREDEFAULTMONSTER:Y` ".

**Note:** The PCGen data team is moving away from using the "Default
Monster" setting.  Default Monster Kits are being used instead.

Bearing all the above rules, procedures and gotchas in mind, lets put
together the stat bonuses for the Solar:

> `BONUS:STAT|STR|18            BONUS:STAT|DEX,CON|10            BONUS:STAT|INT|12            BONUS:STAT|WIS,CHA|14            BONUS:STAT|INT,WIS,CHA|1|PREDEFAULTMONSTER:Y`

For the Ninja Monkey we need to pick stats and then apply the same logic
to them to code into the .lst file.   I think I'll go with final stat
values of\
 STR:17 DEX:18 CON:14 INT:11 WIS:15 CHA:10.  Our list of bonus tags  in
the race file would be:

> `BONUS:STAT|STR|6            BONUS:STAT|DEX|8            BONUS:STAT|CON,WIS|4            BONUS:STAT|STR,INT,WIS|1|PREDEFAULTMONSTER:Y.`

------------------------------------------------------------------------

And we'll end lesson \#5 here. Example files for this lesson can be
found in the [LSTFileClass Lesson file folder
here](http://games.groups.yahoo.com/group/LSTfileclass/files/Lesson%20Files/)
.

Thanks for reading along everyone.

Barak\
 LST Chimp



