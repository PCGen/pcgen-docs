+++
date = "2016-08-01"
title = "Lesson #19: .lst - Companion Modifications"
original_url = "/list/lst-file-class/19-companion-mods.html"

[menu.main]
    identifier = "lst-file-class_19-companion-mods"
    name = "Lesson #19: .lst - Companion Modifications"
    parent = "lst-file-class"
    
+++
By Andrew A. Maitland (LegacyKing)

**File(s) Covered:** <span class="lstfile"> companionmods.lst </span>

**Tags used:**

`      FOLLOWER          ,           COPYMASTERBAB          ,           COPYMASTERCHECK          ,           COPYMASTERHP          ,           FOLLOWERADJUSTMENT          ,           HD          ,           MASTERBONUSRACE          ,           RACETYPE          ,           TYPE          ,           USEMASTERSKILL          ,           BONUS:FOLLOWERS          ,           COMPANIONLIST     `

------------------------------------------------------------------------

Welcome to the LST File Class on Companion\_Mod creation and editing. In
this class we cover the basics tags required to make a complete
companion\_mod file and how the file works. As in all things, this is a
small part of the whole, PCGen works in many parts - Which is why I
cover two tags not part of this file, but must be included to get the
"bigger picture".

#### Style Guide

This LST File Class follows the [LST File Class Style
Guide](/list/lst-file-class/style-guide.html) .

------------------------------------------------------------------------

SECTION 1: How to Create Your Own Companions
--------------------------------------------

There may come a time when you want to make your own special companion
which doesn't match the rules. That's okay. Setting up a new companion
with different powers or grants different bonuses to the master is
acceptable. That is what this section is here for, to guide you through
the process of making your companion - be it a Special Familiar, a War
mount or anything else you might want.

So without further adieu...

### Sample Sly Slink Companion

I have a creature that when I gain have 3 levels, grants me a +2 to my
Hide Skill; at 5th level I can use Shadow Walk once per day. It also
gains 3 hit dice when I reach 3rd and 5th.. Sly Slink is only available
as a Shadow Ferret.

------------------------------------------------------------------------

### Required Tags

#### FOLLOWER

The first tag we're going to look at is <span class="lstobj"> FOLLOWER
</span> , each line generally starts with the Follower tag.

Think of the Follower as sort of a class Tag telling the program what
"level" things happen at. So like we have Class Level Lines to tell
PCGen what is applied at that level and lower so to do we have a tag
called `FOLLOWER` which acts in much the same way.

`FOLLOWER:MonkeyFu=1`

The Follower tag can take variables or Class names. So if MonkeyFu is a
Class then you need to have the first level to qualify, however,
MonkeyFu is a variable, so you need to have this variable of at least 1
to obtain the rest of the benefits derived from the rest of the line.

`FOLLOWER:Paladin=1`

You need to have 1 level in paladin class.

`FOLLOWER:MagicItem=1`

You need to have 1 in a variable name called MagicItem

------------------------------------------------------------------------

#### TYPE

The second and VERY important tag is `TYPE`

Type tells pcgen what applies to this line. The ones used commonly in
PCGen's main sets are: Familiar, Animal Companion, Special Mount, Mount
and Follower.

Any Creature meeting that "TYPE" will have the benefits applied to them.
Simply put without a TYPE PCGen won't be able to able the changes you
code up. TYPE has to match exactly the name from `COMPANIONLIST` . Think
of TYPE as a Group as it groups things together, so with that frame of
mind, Familiar is a group, as is Special Mount.

Example of a Familiar:

`COMPANIONLIST:Familiar|Bat,Cat`

Bat and Cat are both of the Familiar TYPE or group.

------------------------------------------------------------------------

### Miscelaneous Tags

You can use any Tags that are appropriate for your Companion.

The following tags are commonly use on the Follower Line.

------------------------------------------------------------------------

#### COPYMASTERBAB

This tag identifies the companion's Base Attack Bonus (BAB) progression
and can be set to that of its master, by using the `MASTER` parameter,
or you may use a number, variable or formula.

So, if you want your companion to either follow the Master PC's BAB
progression you would use the following tag:

`COPYMASTERBAB:MASTER` (Common for familiars)

If you wanted to set the companion's BAB to %quot;5%quot; no mater what
level the master is, you would use the following tag:

`COPYMASTERBAB:5`

------------------------------------------------------------------------

#### COPYMASTERCHECK:MASTER

That's it, this only copies the Master's Base Checks (Commonly
Fortitude, Reflex and Will) The creature will use it's Stats to modify
the base though (Common for Familiar)

`COPYMASTERCHECK:MASTER`

------------------------------------------------------------------------

#### FOLLOWERADJUSTMENT

This is used appended to the COMPANIONLIST tag. COMPANIONLIST is a Tag
that is not used in a companion mod file. However, it is important to
mention it's uses as it pertains to the companionmod file.

Example from the docs

`COMPANIONLIST:Animal Companion|Ape|FOLLOWERADJUSTMENT:-3`

An Ape companion to a 4th level Druid gains the benefits normally
granted to a companion of a 1st level Druid.

------------------------------------------------------------------------

#### HD

This will grant bonus Hit Die of the creature type.

`HD:5`

Will grant 5 bonus Hit Die (Or class levels) of the creatures type (The
Creature TYPE is called RACETYPE and normally follows the standard
choices. The RACETYPE can be changed inside the CompanionMod lst file
any bonus HD will use that Race Type. If the Creature is Fey it will
gain the HD and class benefits of being 5 HD stronger

NOTE: The base creature can exceed the maximum HD cap for its race in
this manner.

------------------------------------------------------------------------

#### MASTERBONUSRACE

Sets any special bonuses a particular race or creature may grant to the
master (Common for familiar).

Common tags to follow this are BONUS and VFEAT.

The uses of this tag are not to be underestimated, with this tag you can
grant a level dependent bonus to the master at a certain level.

`MASTERBONUSRACE:Bat <TAB> BONUS:SKILL|Spot|3`

Would give the master +3 bonus to Spot checks if he has a Bat.

`MASTERBONUSRACE:Bat <TAB> BONUS:VAR|MyCoolVar|3|PREPCLEVEL:MIN=10`

At 10th level the Master of this Bat gets 3 to his 'MyCoolVar' which can
be attached to a feat, ability, or even an item with a Variable in the
SPROP.

`MASTERBONUSRACE:Magic Item - Sword <TAB> BONUS:VAR|MagicWeaponPlusIncrease|2|PREVARGTEQ:MagicItem,1`

This will grant two (2) to the varaible MagicWeaponPlusIncrease when the
PREVAR requirements are met.

------------------------------------------------------------------------

#### RACETYPE

This tag will change the base creature's type to the one listed.
RACETYPE affects the Bonus HD and progression of the creature.

`RACETYPE:Fey`

The creature now has the Fey Type which replaces its previous RACETYPE
as assigned by the race file.

------------------------------------------------------------------------

#### USEMASTERSKILL

Determines whether the creature will have the exact same skill ranks as
the master.

Your choices are `YES` and `NO` (Default).

`USEMASTERSKILL:YES`

Creature will have the exact same ranks in the skills chosen by the
master.

------------------------------------------------------------------------

#### BONUS:FOLLOWERS

Although this tag is not used in a <span class="lstfile">
companionmods.lst </span> file, it does deserve mention in this class.

The `BONUS:FOLLOWER` tag is what allows us to actually gain a creature
in a particular TYPE or group. Without it you won't be able to select or
add any creatures from that TYPE or group. This needs to match the
`COMPANIONLIST` definition, which is seen as the companion type inside
our actual file.

The following line will be found in your non-companion mod lst file
(e.g. <span class="lstfile"> class.lst </span> , <span class="lstfile">
feat.lst </span> , <span class="lstfile"> race.lst </span> , <span
class="lstfile"> template.lst </span> , etc.)

`BONUS:FOLLOWERS|           Familiar          |1`

You can gain one (1) Familiar

The following line is the corresponding line in the <span
class="lstfile"> companionmod.lst </span> :

`FOLLOWER:Whatever=1 <TAB> TYPE:           Familiar     `

`COMPANIONLIST:           Familiar          |Foo`

Notice the pattern, if you don't match those exactly you won't get
access to that TYPE or group. I bolded the entries for you to see what
must match.

------------------------------------------------------------------------

### Putting it All Together

Okay, lets put together the sample critter

Remember the sample from the begining? "I have a creature that when I
gain have 3 levels, grants me a +2 to my Hide Skill; at 5th level I can
use Shadow Walk once per day. It also gains 3 hit dice when I reach 3rd
and 5th. Sly Slink is only available as a Shadow Ferret.". Well we are
going to make that into something PCGen understands.

> `FOLLOWER:SlySlinkLvl=3 <TAB> TYPE:Sly Slink <TAB> HD:3`
>
> `FOLLOWER:SlySlinkLvl=5 <TAB> TYPE:Sly Slink <TAB> HD:3`

> `MASTERBONUSRACE:Shadow Ferret <TAB> TYPE:Sly Slink <TAB> BONUS:SKILL|Hide|2|PREPCLEVEL:MIN=3 <TAB> SAB:use Shadow Walk once per day|PREPCLEVEL:MIN=5`

In an ability or somewhere else you would need this:

> `FOLLOWERS:Sly Slink|1 <TAB> COMPANIONLIST:Sly Slink|Shadow Ferret <TAB> DEFINE:SlySlinkLvl|0 <TAB> BONUS:VAR|SlySlinkLvl|TL`

Okay, lets put together another sample critter

> `FOLLOWER:Monkey Warrior=1 <TAB> HD:5 <TAB> TYPE:Monkey Mount <TAB> ABILITY:Special Ability|AUTOMATIC|Dodging Foo|Nasty Breath <TAB> RACETYPE:Dragon <TAB> USEMASTERSKILL:YES`

Okay Class, I threw a few curve balls in there. As a 1st level Monkey
Warrior, `FOLLOWER:Monkey Warrior=1` , my critter of the Monkey Mount
type, `TYPE:Monkey Mount` , will become a Dragon race type,
`RACETYPE:Dragon` . It will use my skill rank selection,
`USEMASTERSKILL:YES` , and get the special abilities of Dodging Foo and
Nasty Breath,
`ABILITY:Special Ability|AUTOMATIC|Dodging Foo|Nasty Breath` , as
automatic abilities.

`FOLLOWER:Monkey Warrior=5 <TAB> HD:5 <TAB> SR:12+HD`

When Monkey Warrior becomes 5th level, my critter will gain another 5
bonus hit die and gain Spell Resistance of 12 + it's HD.

This is showing you what is possible in your own Companion Mod file.

Now, we shouldn't leave you at this... You need to place the
COMPANIONLIST tag somewhere outside this file, either a feat, ability,
template or even inside a class, and with the tag you choose what
creatures belong in the Monkey Mount (TYPE) or group.

`COMPANIONLIST:Monkey Mount|Wolf,Fuzzy Bear`

That would make a Wolf and Fuzzy Bear part of the Monkey Mount (TYPE) or
group.

`COMPANIONLIST:Monkey Mount|Bat|FOLLOWERADJUSTMENT:-5`

If my Monkey Warrior takes a bat companion he needs to be 6th level
before the 1st level effect takes place and then 10th level for the
level 5 effect. The '-5' means the creature in that grouping will act as
if five (5) levels lower, this works regardless of Class or Variable.
Druid Class in the SRD and RSRD makes a great example of this case.

Now an advanced technique for those that feel they understand this.

`COMPANIONLIST:Intelligent Item|Intelligent Weapon - Longsword`

`BONUS:FOLLOWERS|Intelligent Item|1`

> `MASTERBONUSRACE:Intelligent Weapon - Longsword <TAB> BONUS:SKILL|Move Silently|5|TYPE=Competence <TAB> AUTO:FEAT|Weapon Focus(Longsword) <TAB> BONUS:VAR|WeaponPlusIncrease|1|PREPCLEVEL:MIN=8`

Can you figure it out? If I have the Intelligent Weapon - Longsword I'll
get a plus five (+5) competence bonus to Move Silently, Weapon Focus for
the Longsword as an Automatic Feat and when I attain a total character
level of eight (8th level) I will get plus one (+1) to the variable name
'WeaponPlusIncrease'. Were you able to follow that? If not, it's okay,
this can become complex quickly.

Okay, that should get you on the path of Companion Mod file creation. In
the next section we discuss applications of adding and modifying the
Companion List.

------------------------------------------------------------------------

SECTION 2: Modifying Companion Lists
------------------------------------

It always happens, either through a feat, new power or just a whim.
Regardless of the source, there may come a time when you wish to add to
the list of available critters to a certain class or group.

`COMPANIONLIST` is additive. A good example of this case is Improved
Familiar.

`COMPANIONLIST:Familiar|Shocker Lizard,Stirge|PRECLASS:1,SPELLCASTER.Arcane=5`

This will grant the Shocker Lizard and Stirge to the available list in
the Familiar (TYPE) if the master is an Arcane Spell Caster of 5th level
or higher.

`COMPANIONLIST:Monkey Mount|Sand Shark`

This will grant the Sand Shark to the available list in the Monkey Mount
(TYPE) group.

------------------------------------------------------------------------

-Andrew Maitland

------------------------------------------------------------------------



