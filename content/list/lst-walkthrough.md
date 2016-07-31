+++
date = "2016-08-01"
title = "PCC and LST Files Explained"
original_url = "/list/lst-walkthrough.html"

[menu.main]
    identifier = "list_lst-walkthrough"
    name = "PCC and LST Files Explained"
    parent = "list"
    
+++
In this section we will be discussing the format of LST and PCC files,
and more importantly, what PCGen expects when parsing LST tags. We will
not be discussing the detailed syntax for each tag. To get more detailed
information about each LST tag, you will need to refer to PCGen's
documentation.

This document follows the System Reference Document (SRD) for 3E. It was
also written based on the early PCGen v5.x data files but has been
updated to the 5.16 data standard. The 5.16 data files are located in
the \\data\\d20ogl\\srd\\ directory of PCGen.

PCGen interprets data files using tabs and line returns. Note that a
return (i.e. hitting the "enter" or "return" key) is different from
word-wrap. You are advised to use a true text editor like the basic
windows Notepad or one of the free editing programs like UltraEdit.
Regardless, turn word-wrap off.

The examples found in this section will use indented lines rather than
the tabs, as are found in actual LST code.

So a line of LST code that looks like this:

Bob &lt;tab&gt; lsttag1 &lt;tab&gt; lsttag2

Alice &lt;tab&gt; lsttag3 &lt;tab&gt; lsttsg4

Will be displayed as:

Bob

lsttsg1

lsttsg2

Alice

lsttsg3

lsttsg4

------------------------------------------------------------------------

What is a PCC file and why are we discussing it first?
------------------------------------------------------

A PCC file is the only way PCGen can see a LST file. Perhaps the most
common problem people have creating their first home brew LST file is
failing to create a PCC that references it.

While most users will only use PCCs as little more than a list of LSTs
for their home brew campaigns, when converting a published source for
PCGen, the PCC file is an expression of the legal system in the form of
the Open Gaming License (OGL). Only through the OGL, other similar
licenses, or through direct licensing from the publishes can PCGen
distribute data from published sources without violating copyrights.
This makes the PCC the most important part element in distributing
copyrighted data.

For a completely original campaign, you are the owner of your material
and the copyrights. You should still declare all the copyright
information, just in case your data files somehow find their way into
distribution. Keep in mind that a PCC is the sole way for PCGen to
identify a LST file and that the structure established for the PCC files
is primarily to fulfill that purpose. The copyright information is for
legal compliance, not program functionality.

------------------------------------------------------------------------

Building your own PCC
---------------------

The PCC file consists of the header block, used to fulfill the legal
obligations of data distribution, provide information used in
prioritizing the data, and identifying which types of games it the data
is compatible with, e.g. Fantasy RPGs, Sci-Fi RPGs, etc., and a main LST
file block that contain a list of LST files that make up the data set.
The PCC file consists of a single entry for each line.

### Where to Find the Files

Typically PCC files are kept within the "data" directory of your PCGen
installation. They can be located in a sub-directory as PCGen will find
all PCC files located within the data directory structure.

Another source for PCC files is the "Vendor Data" directory, specified
in the [Preferences:PCGen:Location](/menu/settings/pcgen/location.html)
dialogue under the Setting menu.

PCC files can also be loaded off of the internet by checking the "Allow
sources to be loaded from web links" checkbox in the
[Preferences:PCGen:Sources](/menu/settings/pcgen/sources.html) dialogue
under the Settins menu. Then you can load sources from a webpage from
the ["Source Material"](/tab/source-tab/source-tab_index.html) Main Tab.

FYou will see included below a sample PCC file. You can see the tags
used and the order in which they are typically found. The order is not
important, except for the first three tags, but following these
conventions will help others help you if you make a mistake. For legal
reasons, few of the header tags should ever be omitted. See the [.pcc
Files tags](/list/data/pcc.html) documentation for a complete listing on
[Data Set and Campaign Information
Tags](/list/data/pcc.html#datasettags)

Sample PCC FIles:

`CAMPAIGN:` - Name of Campaign Displayed in data load window.

`GAMEMODE:3e` - Designates the Game Mode.

`TYPE:Dominant Game Publisher.SRD` - Type will be used for sorting.

`RANK: 1` - Rank indicates priority in sorting.

`GENRE:` - This tells PCGen what genre this is, used to filter sources.

`BOOKTYPE:` - Identifies the source book type for use in prerequisites
for loading other source book.

`SETTING:` - Identifies the setting of which this source is part.

`!PRECAMPAIGN:1,BOOKTYPE=Core Rules` - Established the prerequisite for
loading.

`PUBNAMELONG:The Full Name of the Source` &lt; - Long name for the
publisher of the material (used in some displays).

`PUBNAMESHORT:Source` - Short name for the publisher of the material
(used in some displays).

`PUBNAMEWEB:http://www.mywebsite.com` - Website for the publisher's
site).

`SOURCELONG:The Full Name of the Source` &lt; - Long title (used in some
displays).

`SOURCESHORT:Source` - Short title (used in some displays).

`SOURCEWEB:http://www.mywebsite.com` - Website for the source (typically
the publisher's general site).

`ISOGL:YES` - If the source uses the open gaming license (OGL) See OGL
FAQ.

`COPYRIGHT:Open Game License v 1.0a Copyright 2000, WotC etc.` -
Copyright Terms.

`COPYRIGHT:Full Name of the Source Copyright 2003, Company Name, Authors Names`
- Copyright Owner.

`[LST Type]:[LST File Name]` - Call a LST file.

### LST Types

PCC files specify the type of LST files used in the loaded campaign and
therefore will contain references to multiple LST file object types. In
contrast, LST files are specialized, containing only information on a
single type of LST object.

Types of LST Objects:

-   ABILITY
-   ABILITYCATEGORY
-   ARMORPROF
-   CLASS
-   COMPANION MODIFIER
-   DEITY
-   DOMAIN
-   EQUIPMENT
-   EQUIPMENT MODIFIER
-   FEAT
-   KIT
-   LANGUAGE
-   RACE
-   SHIELDPROF
-   SKILL
-   SPELL
-   TEMPLATE
-   WEAPONPROF

You can also call other PCC files from within a PCC file with the
following:

`PCC:myPCC.pcc` .

If you wanted to call a LST file of "Class" objects named <span
class="lstfile"> myfirstclass.lst </span> , you would have the following
line in your PCC file.

`CLASS:myfirstclass.lst`

For a complete listing of LST file types and the tags used to load them,
see the [PCC Main Body Tags](/list/data/pcc.html#mainbodytags) in
PCGen's LST Tag Dictionary.

#### Data Set File Pathnames

The basic information provided in the previous section assumes the file
<span class="lstfile"> myfirstclass.lst </span> is in the same directory
as the PCC file. If this is not the case, say you wanted this PCC to
load the file <span class="lstfile"> srdspells.lst </span> stored in
<span class="lstfile"> pcgen\\data\\d20ogl\\srd </span> you would use
the following line:

`SPELL:@/d20ogl/srd/srdspells.lst`

The "@" symbol tells PCGen to start at the top of the **data** directory
and then follow the path down.

`CLASS:&/complete_monkey/complete_monkey_classes.lst`

The "&" symbol tells PCGen to start at the top of the **vendor** data
directory and then follow the path down.

The "\$" symbol tells PCGen to start at the top of the **homebrew** data
directory and then follow the path down.

#### Excluding and Including from LST files

You can include or exclude specific information from any LST file by
using the `INCLUDE` or `EXCLUDE` tags.

Examples:

`CLASS:myfirstclass.lst|@/d20ogl/srd/srdclassesbase.lst|(INCLUDE:Fighter)`

Loads the classes in <span class="lstfile"> myclass.lst </span> and the
"Fighter" class from the SRD classes.

`CLASS:myfirstclass.lst|(EXCLUDE:Monk|Sorcerer)|@/d20ogl/srd/srdclassesbase.lst`

Load all classes in <span class="lstfile"> myclass.lst </span> and all
the SRD classes except for the "Monk" and "Sorcerer" classes.

You'll find more information on these and all PCC file tags in PCGen's
[PCC File Tag](/list/data/pcc.html) documentation.

------------------------------------------------------------------------

Building Your Own LST Files
---------------------------

Because LST files are called from PCC files they have little in the way
of a header, just a `SOURCExxx` tag, which provides information used on
character sheets and displays.

LSTs can be complicated in the whole, but are typically quite simple.
Here, in the author's opinion, are the LSTs sorted by complexity. I will
be detailing the assembly of key LSTs at various levels of complexity.

-   language
-   proficiency, be it weapon, armor or shield
-   skill
-   companion modifier
-   deity
-   domain
-   equipmod
-   equipment
-   spell
-   feat
-   race
-   kit
-   template
-   class

The basic construction of a LST is a simple header block followed by a
list of entries and their respective tags. With the exception of the
name the order of tags is flexible but it is best to follow conventions.
Tags are separated by tabs (hit the tab key on your keyboard) or
whitespace. Most entries are on separate lines.

Remember, in these examples I will be using extra lines with indention's
to reflect the tags rather than tabs for readability. Blank lines will
separate entries.

Language LST
------------

This is as basic as it gets. Entries in a language LST are displayed in
the language selection box. It consists of the header and a list of
languages and their type. Let's consider two hypothetical languages, the
spoken language Simian and the written only language Peel.

Here is the header block:

`SOURCELONG:PCGen Documentation`

`SOURCESHORT:P-Doc`

`SOURCEWEB:http://www.pcgen.org`

Here the header tells us in detail where the information came from, a
short name for use in cramped locations, and the website of the source.

Then comes the actual code. In order we list the language name and type.
Most LSTs have more options so with the exception of the name the order
of tags is flexible but it is best to follow conventions. Tags are
separated by tabs (hit the tab key on your keyboard) or whitespace.
Entries are on separate lines.

And here are the two working tags:

`Simian`

`TYPE:Spoken`

`Peel`

`TYPE:Written`

You can refer to the srdlanguages.lst for a working example.

Equipment LST
-------------

Custom equipment is often one of the first things that a GM needs to
create. We'll start with something simple, like a Mighty Sling.

First, the header block:

`SOURCELONG:PCGen Documentation`

`SOURCESHORT:P-Doc`

`SOURCEWEB:http://www.pcgen.org`

Then comes the actual code. In order we list the item's name, type,
cost, weight, sourcepage, proficiency used, crit multiplier, critical
range (i.e. 1 for a 20, 2 for 19-20, etc), damage, range (if ranged
weapon), size, and any bonuses and special abilities. Other than the
name the order is flexible but it is best to follow conventions.

If you create a wholly new weapon with a new proficiency, you will need
to create a proficiency LST that references your new weapon and then
have your PCC load it.

Here is what we end up with, separating each tag into a separate line

`Sling (+1 Mighty)`

`TYPE:Weapon.Simple.Ranged.Standard.Bludgeoning`

`COST:0`

`WT:0`

`PROFICIENCY:Sling`

`CRITMULT:x2`

`CRITRANGE:1`

`DAMAGE:1d4`

`RANGE:50`

`SIZE:S`

`BONUS:WEAPON|DAMAGE|STRMIN1`

Looking at this you might notice the source page tag is missing. Yup,
it's optional and since this is a "home made" item without a sourcebook,
I left it off.

The TYPE tag is fairly easy to read, but you will likely need to refer
to the documentation and srdequip(something).lst for examples.

The BONUS tag is a very, very, very feature rich tag. You will need to
read the docs very carefully. This particular implementation indicates
that it applies only to a weapon, modifies the damage dealt, and adds +1
strength damage to the weapon as long as the user has a strength bonus
of at least +1. A mighty +2 sling would be identical except for the tag

`BONUS:WEAPON|DAMAGE|STRMIN2`

Now lets do something a bit more and create some magical armor. Red
Dragon Armor will be plate +2 that provides fire resistance +5 and makes
the wearer immune to Red Dragon fear. We'll start by copying the plate
armor from the srdequiparmorshields.lst file.

`Full Plate`

`TYPE:Armor.Heavy.Suit.Standard.Metal`

`COST:1500`

`WT:50`

`ACCHECK:-6`

`MAXDEX:1`

`SOURCEPAGE:Chap.7, Armor`

`SPELLFAILURE:35`

`BONUS:COMBAT|AC|8|TYPE=Armor.REPLACE`

Looking at it you can see how its tags work and how similar it is to the
weapons. Name, type, cost, weight, armor check penalty, maximum dex
bonus, source page, percent chance of spell failure, and the armor class
bonus, set up as a replace to ensure only one set of armor is used.

For our custom version we'll be adding some other features. Other
examples can be pulled from the srdequiparmorsheildspecific.lst

`Red Dragon Armor`

`PROFICIENCY:Full Plate`

`TYPE:Magic.Armor.Heavy.Standard.Suit.Specific`

`COST:16650`

`WT:50`

`ACCHECK:-5`

`MAXDEX:1`

`SPELLFAILURE:35`

`BONUS:COMBAT|AC|10|TYPE=Armor.REPLACE`

`SAB:Fire Resistance +5`

`SAB:Immune to Red Dragon Fear`

Notice the changes?

First we added a PROFICIENCY tag - Very important as it informs PCGen
which characters can use the armor since the name no longer matches any
of the armor use proficiencies.

The TYPE also changes to include Magic and Specific. Magic will always
be flagged first, the Specific tells it that it is a named item.

Then there's the reduced ACCHECK rating. Why? Well, all magic items are
masterwork, and masterwork armor has a reduced armor check penalty.

Last, the AC bonus was increased by 2 in the BONUS tag. The cost is my
personal evaluation of the cost of this armor.

For armor found in a horde you may be tempted to set it to 0 so they can
buy it without hitting the "buy for free" tag, but it is recommended to
set the cost so you can use the "owned wealth" calculation to make sure
your PCs have as much, or as little, as you think they should.

Last come the SAB tags. SAB stands for Special Ability and reflects a
text string that is displayed on the character sheet. SABs have no
affect on PCGen's operation. SABs can be used as requirements and can
perform calculations (like displaying uses per level). SABs are almost,
but not quite, as feature rich as BONUS. Remember citizen, the docs are
your friends.

Proficiency LST
---------------

Proficiency lst files come in tree type: Armor, Shield, and Weapon. We
will look at each if these, starting with the last, which also is the
most complicated.

### Weapon Proficiency LST

For completeness I have included an example of a weapon proficiency
below with the most complicated proficiency in the basic game; the
bastard sword.

From your reading you should be aware that by the Martial Weapon
proficiency, a person can use the sword two handed if medium sized, or 1
handed if they are a Large (or larger) creature. Only someone who has
the Exotic Weapon Proficiency for the Bastard Sword can use it one
handed.

Cannibalizing the <span class="lstfile"> srd\_weaponprofs.lst </span>
file we get:

`SOURCELONG:PCGen Documentation`

`SOURCESHORT:P-Doc`

`SOURCEWEB:http://www.pcgen.org`

`Sword (Bastard)`

`TYPE:Martial.Exotic.Sword`

So you see the weapon's name, the type, and the number of hands required
to use the weapon. If you don't specify the number of hands, PCGen's
sizing system automatically fires up, assigning weapons of same or
smaller size to 1 hand use, and weapons sized larger than the character
to 2 hand use.

In this case, the Martial version of the proficiency does NOT allow a
medium creature to use the medium sized Bastard Sword one-handed and
overrides the default.

The Exotic version follows the standard PCGen sizing system which works
as the rules require.

Refer to the HANDS tag docs for more details.

### Armor Proficiency LST

### Shield Proficiency LST

Feat LST
--------

Feats are handy things. They have a lot of power, but are really fairly
simple. We'll start at the beginning of the srdfeats.lst and pull
alertness.

`Alertness`

`TYPE:General`

`DESC:See Text`

`BONUS:SKILL|Listen,Spot|2`

`SOURCEPAGE:Chap.5, Feat Descriptions`

So we have the name, type, description, a bonus of +2 to listen and
spot, and sourcepage. Really the name, type and description are the only
things you need. Some feats provide features that are not handled in
PCGen because they are conditional or just not addressed.

We'll move on to something meatier.

`Weapon Specialization`

`TYPE:Special.Fighter`

`PREFEAT:1,Weapon Focus`

`PREVARGTEQ:WeapSpecQualify,1`

`DESC:See Text`

`MULT:YES`

`CHOOSE:FEAT=Weapon Focus|1`

`BONUS:WEAPONPROF=%LIST|DAMAGE|2|TYPE=NotRanged`

`BONUS:WEAPONPROF=%LIST|DAMAGE-SHORTRANGE|2`

`SOURCEPAGE:Chap.5, Feat Descriptions`

A bit different, but not much. Besides the normal stuff, we see that
Weapon Specialization requires the character to already have the feat
Weapon Focus and have a variable called WeaponSpecQualify with a value
of 1. We'll see WeaponSpecQualify later in the CLASS section where it
will be covered in more detail. It can be chosen MULTiple times but only
once per weapon, a feature inherent in PCGen. You CHOOSE a weapon that
you already have Weapon Focus and it receives a +2 to damage.

Race LST
--------

Races are a step up the complexity list from feats. We'll first examine
one of the most complex standard races, at least by PCGen standards, the
Elf. This, and other examples, can be found in the srdracesphb.lst file.

`Elf`

`FAVCLASS:Wizard`

`STARTFEATS:1`

`SIZE:M`

`MOVE:Walk,30`

`REACH:5`

`VISION:Low-light`

`LANGAUTO:Common,Elven`

`LANGBONUS:Draconic,Gnoll,Gnome,Goblin,Orc,Sylvan`

`WEAPONAUTO:Shortbow|Longbow|Longbow (Composite)|Shortbow (Composite)`

`WEAPONBONUS:Rapier|Longsword`

`BONUS:SKILL|Listen,Search,Spot|2|TYPE=Racial`

`BONUS:STAT|DEX|2`

`BONUS:STAT|CON|-2`

`SAB:Immunity to magic sleep spells and effects`

`SAB:+2 racial saving throw bonus against Enchantment spells or effects`

`SAB:An elf who merely passes within 5 feet of a secret or concealed door is entitled to a Search check to notice it as if she were actively looking for the door`

`TYPE:Humanoid`

`SOURCEPAGE:Chap.2, Elves`

What we find is the race name, favored class, number of starting feats,
size, movement types and speeds, reach, special vision types, automatic
languages, the list of available bonus languages, automatic weapon
proficiencies, a bonus proficiency that is chosen in the race window,
racial adjustments to skills and stats (note the Con penalty applied as
a negative bonus), followed by special abilities, the creature type and
source page. Notice the SABs with nice, descriptive tags.

Since SABs have no affect on PCGen, you should make sure the relevant
data is in the SABs. (Unless the copyright owner says not to. You'll
find lots of things with an SAB of "Super Power: see text p.xx" because
the publisher doesn't want Super Power defined outside their books. It's
their book, it's their right and we respect that. Do what you want for
your own creations.)

The required entries are name, size, movement, reach, and creature type.
Everything else is optional and there are many, many more racial tags
available for use.

Our example race will be a Silverback, a strong and intelligent creature
(+2 strength, +1 intelligence) but somewhat inflexible (dexterity -1),
they are Large creatures with a 10' reach, 60' darkvision, bonuses to
handle animal, diplomacy and sense motive (+2 each), immune to charm
spells, with a preferred class of ranger. They automatically speak
Simian and Common and have an elf-like list of bonus languages. Like
most races, they only receive 1 feat at first level. Silverbacks have no
automatic weapon proficiencies but they do get two claw attacks doing
1d6 damage. Silverbacks do not receive any bonus hit dice or have
monster classes.

Building our race.lst file from scratch we put our standard header.

`SOURCELONG:PCGen Documentation`

`SOURCESHORT:P-Doc`

`SOURCEWEB:http://www.pcgen.org/`

`Silverback`

`FAVCLASS:Ranger`

`STARTFEATS:1`

`SIZE:L`

`MOVE:Walk,30`

`REACH:10`

`VISION:Darkvision (60')`

`LANGAUTO:Common,Simian`

`LANGBONUS:Draconic,Gnoll,Gnome,Goblin,Orc,Sylvan,Elven`

`BONUS:SKILL|Handle Animal,Diplomacy,Sense Motive|2|TYPE=Racial`

`BONUS:STAT|STR|2`

`BONUS:STAT|INT|1`

`BONUS:STAT|DEX|-1`

`NATURALATTACKS:Claw,Weapon.Natural.Melee.Piercing.Slashing,*2,1d6`

`SAB:Immunity to charm`

`TYPE:Humanoid`

The differences between this and the Elf are primarily the missing
weapon bonuses and the new NATURALATTACKS tag. NATURALATTACKS do not
need a proficiency specified so no worries there. You can see it is
called Claw, is a natural melee piercing/slashing weapon and there are
two of them.

More complex races abound in the SRD directory. Consider examining the
srdracesXXX.lst files. Srdracesst.lst includes tritonss, troglodytes and
trolls which are good examples for player character races.

Class LST
---------

After custom equipment, classes are the most popular new LST. They are
also perhaps the most complicated and difficult to master. Mastery takes
time, but most people can achieve sufficiency in a very short period of
time. And sufficiency is, well, sufficient.

The first barrier to overcome is that class LSTs do not follow the one
line per entry system that all the other LSTs follow. Classes are too
complicated to do that. So you have three sections to a class entry: a
combat definition, a skill set definition, and the level-specific
events.

Some will have more sections to cover special functions, but these are
the standards. Once you start the level-specific block you can put
entries in whatever order you want or have multiple entries for the same
level. All those entries will apply until it finds a new definition
block.

We'll begin simple and look at the Warrior, your basic muscle. Like the
other examples, blank lines indicate a new line and the indentions list
the tags that fall on that line.

`CLASS:Warrior`

`CLASS:Warrior`

`HD:8`

`TYPE:NPC`

`ABB:War`

`SOURCEPAGE:Chap.2, Classes, NPC Classes`

`BONUS:CHECKS|BASE.Fortitude|CL/2+2`

`BONUS:CHECKS|BASE.Reflex,BASE.Willpower|CL/3`

`BONUS:COMBAT|BAB|CL`

`CLASS:Warrior`

`STARTSKILLPTS:2`

`CSKILL:Climb|Handle Animal|Intimidate|Jump|Ride|Swim`

`1`

`WEAPONAUTO:SIMPLE|MARTIAL`

`AUTO:FEAT|:Simple Weapon Proficiency|Armor Proficiency (Light)|Armor Proficiency (Medium)|Armor Proficiency (Heavy)|Shield Proficiency|Martial Weapon Proficiency`

In the combat definition we find hit dice, class type (base, prestige,
NPC, monster, etc), abbreviation to be used, source page, saving throws
and base attack bonus.

The skill set block covers class skills and skill points per level. The
skill names in the block need to match the entries in the skill LST
file.

The level specific block only addresses first level where we see the
warrior receives all simple and martial weapon proficiencies and all
armor and shield proficiencies.

Notice that all the definition blocks start with CLASS:. This is the
keyword used by PCGen. Leave that out and bad things will happen.

To make a warrior into a fighter we'd change the hit die and add some
more level-specific abilities, specifically feats. Here is the level
specific block for the fighter from the srdbaseclasses.lst file:

  ------------------------------------ ------------------------------------
  `1`                                  `ADD:FEAT(TYPE=Fighter)`

                                       `WEAPONAUTO:SIMPLE|MARTIAL AUTO:FEAT
                                       |:Armor Proficiency (Light)|Armor Pr
                                       oficiency              (Medium)|Armo
                                       r Proficiency (Heavy)|Shield Profici
                                       ency|Simple Weapon Proficiency`
  ------------------------------------ ------------------------------------

  ----- --------------------------
  `2`   `ADD:FEAT(TYPE=Fighter)`
  ----- --------------------------

  ------------------------------------ ------------------------------------
  `4`                                  `DEFINE:WeapSpecQualify|1`
                                       `ADD:FEAT(TYPE=Fighter)`
  ------------------------------------ ------------------------------------

  ----- --------------------------
  `6`   `ADD:FEAT(TYPE=Fighter)`
  ----- --------------------------

  ----- --------------------------
  `8`   `ADD:FEAT(TYPE=Fighter)`
  ----- --------------------------

  ------ --------------------------
  `10`   `ADD:FEAT(TYPE=Fighter)`
  ------ --------------------------

  ------ --------------------------
  `12`   `ADD:FEAT(TYPE=Fighter)`
  ------ --------------------------

  ------ --------------------------
  `14`   `ADD:FEAT(TYPE=Fighter)`
  ------ --------------------------

  ------ --------------------------
  `16`   `ADD:FEAT(TYPE=Fighter)`
  ------ --------------------------

  ------ --------------------------
  `18`   `ADD:FEAT(TYPE=Fighter)`
  ------ --------------------------

  ------ --------------------------
  `20`   `ADD:FEAT(TYPE=Fighter)`
  ------ --------------------------

Pretty simple. Only the 4 ^th^ level DEFINE statement should require
explanation. The DEFINE statement is used to initialize a variable, in
this case WeapSpecQualify, and set it to 1. This is the prerequisite for
the Weapon Specialization feat we saw earlier.

Let's look at something more magical, like a bard.

`CLASS:Bard`

`HD:6`

`SPELLSTAT:CHA`

`SPELLTYPE:Arcane`

`TYPE:Base.PC`

`ABB:Brd`

`MEMORIZE:NO`

`SOURCEPAGE:Chap.3, Bard`

`LANGAUTO:Literacy`

`BONUS:CHECKS|BASE.Fortitude|CL/3`

`BONUS:CHECKS|BASE.Reflex,BASE.Willpower|CL/2+2`

`BONUS:COMBAT|BAB|CL*3/4`

Standard combat definition block, but for the Bard it indicates the
class can cast arcane spells using Charisma as the prime stat without
memorizing spells.

`CLASS:Bard`

`PREALIGN:3,4,5,6,7,8`

Bards have an alignment restriction of "non-lawful". The numbers 0-9
correspond to the alignments with the omitted 1, 2, and 9 being lawful
good, lawful neutral and lawful evil respectively.

`CLASS:Bard`

`STARTSKILLPTS:4`

`CSKILL:Alchemy|Appraise|Balance|Bluff|Climb|Concentration|TYPE.Craft| Decipher Script|Diplomacy|Disguise|Escape Artist|Gather Information|Hide| Intuit Direction|Jump|TYPE.Knowledge|Listen|Move Silently|Perform|Pick Pocket| TYPE.Profession|Scry|Sense Motive|Speak Language|Spellcraft|Swim|Tumble|Use Magic Device`

Standard skill set. Nothing to see here, move along.

  ------------------------------------ ------------------------------------
  `1`                                  `CAST:2`

                                       `KNOWN:4`

                                       `SAB:Bardic music %/day|BardicMusic`

                                       `SAB:Bardic knowledge (+%)|BardicKno
                                       wledge`

                                       `BONUS:VAR|BardicMusic|CL=Bard`

                                       `BONUS:VAR|BardicKnowledge|CL=Bard+I
                                       NT`

                                       `DEFINE:BardicKnowledge|0`

                                       `DEFINE:BardicMusic|0`

                                       `WEAPONAUTO:SIMPLE`

                                       `WEAPONBONUS:Longbow|Longbow(Composi
                                       te)|Longsword|Rapier|Sap|Shortbow (C
                                       omposite)|Sword (Short)|Shortbow|Whi
                                       p`

                                       `AUTO:FEAT|:Armor Proficiency (Light
                                       )|Armor Proficiency (Medium)|Shield 
                                       Proficiency|Simple Weapon Proficienc
                                       y`
  ------------------------------------ ------------------------------------

Now we see some new things other than the standard proficiencies and
feats. A first level Bard can cast 2 1 ^st^ level spells and knows four
of them. He has the special ability to use Bardic Music a number of
times equal to his class level (CL) which is handled by an SAB entry
(with % being used to display the value of the BardicMusic variable), a
DEFINE and a BONUS to set the variable to the Bard class level. The same
is done with the Bardic Knowledge bonus.

  ------------------------------------ ------------------------------------
  `2`                                  `CAST:3,0`
                                       `KNOWN:5,2`
  ------------------------------------ ------------------------------------

Bards can now cast 2 ^nd^ level spells (if they have any bonus spells
from their spell-stat Charisma) and know 2 of them.

  ------------------------------------ ------------------------------------
  `3`                                  `CAST:3,1`
                                       `KNOWN:6,3`
  ------------------------------------ ------------------------------------

  ------------------------------------ ------------------------------------
  `4`                                  `CAST:3,2,0`
                                       `KNOWN:6,3,2`
  .                                    
  .                                    
  .                                    
  .                                    
  `20`                                 `CAST:4,4,4,4,4,4,4`
                                       `KNOWN:6,5,5,5,5,5,4`
  ------------------------------------ ------------------------------------

------------------------------------------------------------------------



