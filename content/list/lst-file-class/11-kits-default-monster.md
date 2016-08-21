+++
date = "2016-08-01"
title = "Lesson #11: .lst - Default Monster Kits"
original_url = "/list/lst-file-class/11-kits-default-monster.html"

[menu.main]
    identifier = "lst-file-class_11-kits-default-monster"
    name = "Lesson #11: .lst - Default Monster Kits"
    parent = "lst-file-class"
    
+++
By Aaron Divinsky (boomer70).

**File(s) Covered:** \*kit\_races.lst

**PCGen LST Standard:** PCGen 6.00.x

**GameMode:** 3.5e (RSRD)

**Tags used:**

`      STARTPACK          ,           PRExxx          ,           EQUIPBUT          ,           VISIBLE          ,           RACE          ,           NAME          ,           GENDER          ,           ALIGN          ,           STAT           SKILL           RANK           COUNT           FREE     `

------------------------------------------------------------------------

This lesson is intended to cover creating your own "Default Monster
Kits".  Default Monster Kits are used to encode the information about
the default version of a monster as provided in the source material.

The first thing to note is that a different file set is used when
creating Default Monster Kits than when creating the monster.  The files
in question are called "Starting Kits" or just Kits for short.  Kit
files have a slightly different syntax than other LST files you may
already be familiar with.

The format for a Kit file is each Kit starts with a `STARTPACK` tag and
ends when the code sees another `STARTPACK` tag or the end of file. 
Most tags in a Kit file appear one to a line as opposed to tab separated
as in other list files.  However, there are some tags which require
multiple tags per line and these tags **do** need to be tab separated.

This lesson is not intended as a treatise on Kit files in general.  As
always, see the documentation for more information on [Starting
Kit](/list/data/startingkits.html) file tags.

We will revisit our friends the Solar and the Ninja Monkey that we
created in the previous lessons on races and use them as examples in
this lesson as well.

------------------------------------------------------------------------

[**`STARTPACK`**](/list/data/startingkits/startpack.html)

This tag defines the name of the Kit and also demarcates the beginning
of a new Kit.  By convention we use "Default &lt;Monster name&gt;" as
the name for a default monster kit.

The Solar's entry would be:

> `STARTPACK:Default Angel (Solar)`

The entry for the Ninja Monkey will be:

> `STARTPACK:Default Ninja Monkey`

------------------------------------------------------------------------

**`PRExxx`**

Several items can appear on a `STARTPACK` line. One of those things is a
prereq for anyone to be able to take that kit.  All global prereqs are
allowable on this line.

For default monsters we want to make sure that only a character with a
matching race or no race selected can take the kit.  We don't want those
pesky Ninja Monkeys selecting our Default Angel (Solar) kit.

To do this we will add a [`PRERACE`](/list/global/pre/prerace.html) tag
to the `STARTPACK` line we started above. So we enter a few tabs and
type:

> `PRERACE:1,Angel (Solar)`

However, we also want to allow new characters without a race to select
this Kit. To do this we need to add a new tag to the prereq.  To have
multiple prereqs we need to use the `PREMULT` .  To specify that only a
character without a race can select the Kit we use the syntax "
`!PRERACE:%` ".   So the final tag for the Solar would be:

> `PREMULT:1,[PRERACE:1,Angel (Solar)],[!PRERACE:1,%]`

The tag will be very similar for the Ninja Monkey.

> `PREMULT:1,[PRERACE:1,Ninja Monkey],[!PRERACE:1,%]`

------------------------------------------------------------------------

[**`EQUIPBUY`**](/list/data/startingkits/equipbuy.html)

This tag is used to set the percentage of list price that creatures
applying this kit must pay for equipment added through the kit. 
Monsters are generally granted the equipment listed in the race write up
for free so we generally want to set this to "0" meaning the equipment
is granted for free.

The code to do this would be (also on the `STARTPACK` line):

> `EQUIPBUY:0`

------------------------------------------------------------------------

[**`VISIBLE`**](/list/data/startingkits/visible.html)

This tag allows us to control the visibility of the Kit in the user
interface.  This tag is also specified on the `STARTPACK` line. We want
anyone who is qualified (met the prerequisites we specified earlier) to
take the kit to see it so we will enter "QUALIFY" as the visibility. We
could also specify "YES" or "NO" to control the visibility of the kit.

> `VISIBLE:QUALIFY`

------------------------------------------------------------------------

[**`RACE`**](/list/data/startingkits/race.html)

The next tag we will cover is the `RACE` tag.  As you may have guessed
this allows us to set the race of the character applying the kit.  Now
because setting a character's race to a race it already is can cause
problems in PCGen we want to only set the race if the character doesn't'
already have one (all other scenarios were excluded by the prereqs we
entered earlier for the Kit).

This brings up an important point to note, any kit line can be qualified
with a `PREXXX` tag.  In our case we will use part of the prereq we
entered for race above.

> `RACE:Angel (Solar)<tab>!PRERACE:1,%`

This tells the program execute this line to set the character's race to
Angel (Solar) only if the character doesn't already have a race
selected.  For the Ninja Monkey just replace Angel (Solar) with Ninja
Monkey in the above line.

------------------------------------------------------------------------

[**`NAME`**](/list/data/startingkits/name.html)

Generally, we set the name of the monster character to the name of the
monster exactly as it appears in the source.  We use the `NAME` to
accomplish that.

> `NAME:Solar`

------------------------------------------------------------------------

[**`GENDER`**](/list/data/startingkits/gender.html)

Sometimes a particular monster always has a certain gender, or no gender
at all.  Neither the Solar nor the Ninja Monkey specify a particular
gender so we will skip this tag for them

Just to illustrate if you wanted to create a special female version of
the Solar you could specify `GENDER:Female` on either the `NAME` line or
on its own line.

------------------------------------------------------------------------

[**`ALIGN`**](/list/data/startingkits/align.html)

Next up is alignment.  Obviously if the creatures specifies that it is
"Always" a particular alignment you can simply specify that in the Kit
and any characters created using the kit will have the appropriate
alignment.

The Solar specified that they are "Always Good (Any)".  We can code that
in a Kit as follows:

> `ALIGN:LG|NG|CG`

This will present a chooser to the user when the kit is applied allowing
them to select one of the three specified alignments.

If you remember back to our earlier lesson, we did not all a PREALIGN
for the Ninja Monkey because they were listed as "Usually Chaotic
Good".  Since we are creating a kit for the "usual" case (default) we
will specify Chaotic Good as the alignment for our Default Ninja Monkey.

> `ALIGN:CG`

------------------------------------------------------------------------

[**`STAT`**](/list/data/startingkits/stat.html)

With this tag we can set a character's base stats.  For default monsters
the logic is the base stat is 10 unless the value listed in the write up
is odd in which case the base stat is 11.  Occasionally, a creature
write up will specify that the monster uses a different set of stats,
usually the non-elite array.

It is a good idea to explicitly set each stat a default monster
possesses (is not a nonability) because otherwise a users preference
will be used.

Returning to our examples the `STAT` line for the Solar would look like:

> `STAT:STR=10|DEX=10|CON=10|INT=11|WIS=11|CHA=11`

Our Ninja Monkey has stats of Str 17, Dex 18, Con 14, Int 11, Wis 15,
Cha 10 so our stat line looks like:

> `STAT:STR=11|DEX=10|CON=10|INT=11|WIS=11|CHA=10`

------------------------------------------------------------------------

[**`SKILL`**](/list/data/startingkits/skill.html) /
[**`RANK`**](/list/data/startingkits/rank.html) /
[**`COUNT`**](/list/data/startingkits/count.html) /
[**`FREE`**](/list/data/startingkits/free.html)

This set of tags, which must appear on the same line, allows you to buy
skill ranks in a skill for the character applying the kit. All of the
comments under the section for
[`BONUS:SKILLRANK`](/list/global/bonus/skillrank.html) apply here as
well, except that the workaround for skills which require a choice is
not required. To handle a choice of skills in a default kit we enter all
the choices separated by a pipe (|) character. We then use the special
tag `COUNT` to specify how many choices from the list the character
should get. You can specify specific skills or types of skills like
`TYPE=Knowledge` .

The skills are granted exactly as if you had picked them from the user
interface. The character must have sufficient skill points to buy the
listed skills. Occasionally a source will grant more ranks than the
monster can actually pay for. In these cases you have two options. You
can either not grant the ranks and note that the source appears to be in
error or you can use the `FREE:YES` tag on the **SKILL** line to grant
the extra ranks for "free" (no skill points will be spent).

The kit will also enforce the user preference for Max Ranks for a skill.
Sometimes in order to get the listed total bonus to a skill it would be
necessary to grant more ranks than the max ranks for a skill. Usually
this happens with cross-class skills. To allow the skill to go above the
maximum you can set the "Bypass Max Skill Rank" setting in the PCGen
preferences.

With all that being said our we would add the following lines to our
Solar kit (each SKILL/RANK pair should be on a new line, replace `TAB`
with a real tab character):

> `SKILL:Diplomacy <tab> RANK:23            SKILL:Concentration <tab> RANK:25            SKILL:Escape Artist <tab> RANK:25            SKILL:Hide <tab> RANK:25            SKILL:Listen <tab> RANK:25            SKILL:Move Silently <tab> RANK:25            SKILL:Search <tab> RANK:25            SKILL:Sense Motive <tab> RANK:25            SKILL:Spellcraft <tab> RANK:21            SKILL:Spot <tab> RANK:25            SKILL:TYPE=Knowledge|TYPE=Craft <tab> RANK:25 <tab> COUNT:5      `

Our Ninja Monkey will be very similar:

> `SKILL:Hide <tab> RANK:4            SKILL:Listen <tab> RANK:3            SKILL:Move Silently <tab> RANK:4            SKILL:Spot <tab> RANK:3      `

------------------------------------------------------------------------

[**`FEAT`**](/list/data/startingkits.html#feat) /
[**`FREE`**](/list/data/startingkits/free.html)

The `FEAT` tag is a very simple one. It simply lists each feat a
creature gets one to a line. The `FREE:YES` tag can be added to the
**FEAT** line, as it was done on the **SKILL** line above, to grant the
feat without charging the feat pool. This would primarily useful if a
creature has more feats than it should for its HD.

Our Solar is fairly straightforward. The code appears below.

> `FEAT:Cleave            FEAT:Dodge            FEAT:Great Cleave            FEAT:Improved Initiative            FEAT:Mobility            FEAT:Power Attack      `

------------------------------------------------------------------------

[**`GEAR`**](/list/data/startingkits/gear.html) /
[**`EQMOD`**](/list/data/startingkits/eqmod.html) /
[**`SIZE`**](/list/data/startingkits/size.html) /
[**`LOCATION`**](/list/data/startingkits/location.html)

The last set of tags we need to cover to complete our Solar and Ninja
Monkey examples are the `GEAR` tags.  The Solar gets two pieces of
equipment by default, a +5 dancing vorpal greatsword and a +2 mighty (+5
Str) composite longbow.  To enter this into the kit we first grant the
base item with the `GEAR` tag like so: `GEAR:Greatsword` .

Then we need to add the special abilities to the base item.  We do this
by adding EQMODs just like using the equipment customizer.  For the
greatsword we need to add the following EQMODs: **MWORKW** , **PLUS5W**
, **DANCE** , and **VORPAL** . So we will add the following code to the
**GEAR** line we created earlier: `EQMOD:MWORKW.PLUS5W.DANCE.VORPAL` .

Now we need to make sure that the item is the correct size for the
creature we are creating.  By default, PCGen creates all items at Medium
size.  Our Solar however is a Large size creature so we want his
greatsword to be Large as well.  We can do this with the `SIZE` tag. 
The `SIZE` tag takes the single character abbreviation for size or a
special tag `PC` to size the item to whatever size the character is.  We
will add the `SIZE:PC` tag to our **GEAR** line to make sure that the
Solar's greatsword grows if it does (by adding HD).

The last thing we need to do is equip the item.  If we do not equip the
item the gear will be added to the character as a possession but will
not be used.  This could be useful for items left in the monster's lair
but in our case we actually want the Solar to use its greatsword.  To do
this we use the `LOCATION` tag.  This tag uses the same locations as you
would see in the user interface when equipping an item.  A greatsword is
a two-handed weapon so it can only be equipped to one place "Both
Hands".  We add the tag `LOCATION:Both Hands` .  For items that are not
weapons that can only be equipped to one place on the body (like a ring)
you can simply specify "Equipped" in the `LOCATION` tag and PCGen will
equip it to the correct location.

Now if we put it all together, our kit lines for the Solar's equipment
will look like this:

> `GEAR:Greatsword <tab> EQMOD:MWORKW.PLUS5W.DANCE.VORPAL <tab> SIZE:PC <tab> LOCATION:Both Hands            GEAR:Longbow (Composite) <tab> EQMOD:MWORKW.BOWSTR|5.PLUS2W <tab> SIZE:PC <tab> LOCATION:Carried`

------------------------------------------------------------------------

Well, this brings to a close the lessons on creating monster kits for
use in PCGen. There is much more you can do with kits. I encourage you
to check out the documentation for more in depth information on
everything kits can do.

Aaron, Docs 2nd

------------------------------------------------------------------------



