+++
date = "2016-08-01"
title = "Lesson #17: .lst - Converting Feats to Abilities, The Basic Conversion"
original_url = "/list/lst-file-class/17-converting-feats-to-abilities.html"

[menu.main]
    identifier = "lst-file-class_17-converting-feats-to-abilities"
    name = "Lesson #17: .lst - Converting Feats to Abilities, The Basic Conversion"
    parent = "lst-file-class"
    
+++
By Andrew A. Maitland (LegacyKing) and Eric C Smith (Maredudd)

**File(s) Covered:** <span class="lstfile"> \*abilities.lst </span> ,
<span class="lstfile"> \*feat.lst </span> , <span class="lstfile">
\*.pcc </span> , <span class="lstfile"> \*abilitycategory.lst </span> ,
<span class="lstfile"> miscinfo.lst </span>

**PCGen LST Standard:** PCGen 6.00.x

**GameMode:** 3.5e (RSRD)

**Tags used:**

`      CATEGORY(ability)          ,           PREABILITY          ,           ABILITY(pcc)          ,           ABILITYCATEGORY(pcc)          ,           ABILITYCATEGORY(ability category)          ,           CATEGORY(ability category)          ,           PLURAL          ,           EDITABLE          ,           EDITPOOL          ,           FRACTIONALPOOL          ,           POOL          ,           VISIBLE          ,           DEFINE          ,           TYPE          ,           PRESKILL          ,           PREVARLT          ,           DESC          ,           BONUS:VAR     `

------------------------------------------------------------------------

Introduction
------------

Beginning with PCGen 5.12, and maturing in PCGen 5.14, the Ability
object has been available to the lst monkey as a more flexible tool than
the existing Feat object. Though it was originally conceived as a
replacement for the Feat, it will take quite some time before the Feat
actually goes away, if it ever does.

This lesson will assist users in converting their existing homebrew
feats to the new Ability object. To accomplish this, the lesson is
broken into two sections, the Basic Conversion and the Advanced
Conversion. Within each of these sections you will find discussion of
each file that must be modified, and the tags required to accomplish the
conversion of your homebrew feats.

NOTE: Standard practice in PCGen distributed datasets is to only use the
ability object for those abilities that had been implemented as hidden
feats. Feats listed in the sourcebooks as feats are implemented with the
standard feat object.

What this lesson will not tell you is how to create either Feats or
Abilities. Both are very similar in construction, using the same set of
general tags to provide the functionality required to implement the
various game rules used. The primary difference is that each **ABILITY**
is assigned to a specific **CATEGORY** . This means that you can have
several abilities with the same name, but each will be of a separate
category. The tags required to do this are covered below.

### Sample Feat

The <span class="lstobj"> Expert Defense </span> hidden feat, included
below, will be used as our example in this LST file class.

`Expert Defense`

`TYPE:Special`

`VISIBLE:NO`

`SAB:Expert Defense ~ Add % bonus to AC|INT`

`BONUS:COMBAT|AC|INT`

Note: This hidden feat has been created specifically for this LST File
class.

### Before We Begin

#### File Names

You will see several LST files referenced within this lesson. The file
names used are generic file names and do not represent what your files
will need to be called. The general convention used for official
datasets within PCGen can be found in the [Official Release
Standards](/list/lst-standards.html) . You are free to call your
homebrew datasets by what name you will, though I find it helps to
include the object type contained within the file in the name of the
file. For the purposes of this LST File class, we will use the following
file names:

<span class="lstfile"> my\_abilities.lst </span> file for the converted
abilities.

<span class="lstfile"> my\_abilitycategories.lst </span> file for the
new ability categories.

<span class="lstfile"> my\_campaign.pcc </span> file for the campaign
pcc file.

Note: You can name your homebrew files anything you wish as long as you
include them in the your homebrew PCC file.

#### LST File Class Style Guide

Because HTML formatting cannot exactly replicate what you would see in a
LST file we are going to use certain conventions to convey these ideas:

1\) Coding examples and PCGen tags are identified by `code` style.

2\) When referencing a specific PCGen object, e.g. domain, feat, weapon,
etc., I have included the name as a <span class="lstobj"> LST Object
</span> text, except for when the object is part of a `code` example.

3\) Each new line should be considered a `<TAB>` in the actual file.

> Examples in this lesson will appear as:
>
> `ABILITYCATEGORY:My Special Ability Category`
>
> `CATEGORY:Special Ability`
>
> Will in the LST file appear as:
>
> `ABILITYCATEGORY:My Special Ability Category` &lt;tab&gt;
> `CATEGORY:Special Ability`

#### Special Note for the LST Student

Finally, for those of you that have gone through the previous LST
Classes, some of the global tags will be repetitive. Feel free to skip
those portions if you like. These classes are being written for the new
LST-Monkey, so there will be some overlap, but a student of the classes
does not need to take them in order.

------------------------------------------------------------------------

The Conversion
--------------

The basic process of converting "Feats" to "Abilities" is to create a
new file called <span class="lstfile"> my\_abilities.lst </span> and
then copy the homebrew feats that you wish to convert to the new file
and removing them from the <span class="lstfile"> my\_feats.lst </span>
file. You will then need to add the appropriate `CATEGORY` tag to the
copied feats, making sure that any new ability categories are properly
defined in the <span class="lstfile"> my\_abilitycategories.lst </span>
file. The next step is to modify your hombrew <span class="lstfile">
my\_campaign.pcc </span> file by adding the `ABILITY` and
`ABILITYCATEGORY` tags. The relevant files and tags to acomplish this
are explained below.

------------------------------------------------------------------------

### The Ability File

The <span class="lstfile"> my\_abilities.lst </span> file is where your
converted feats will be placed. Fortunately, the tags you use in this
file are very similar to those used in the <span class="lstfile">
feats.lst </span> file. The major difference between these two files is
that you will need to add the `CATEGORY` tag to your converted feat to
make it an ability. To get an idea of how to build feats, you can look
up [LST File Class \#12](/list/lst-file-class/12-feat-1.html) and [LST
File Class \#13](/list/lst-file-class/13-feat-2.html) , Feat LST Classes
Parts 1 and 2. There will eventually be a LST FIle Class for Abilities
so you can check back periodically to see if it's been released yet.

------------------------------------------------------------------------

#### &lt;Ability Name&gt;

Every ability line must begin with the name of the ability. You can use
any name you prefer as long as it conforms to the standard requirements
for feat names. For our purposes in this class, we will be using the
same name we used for our sample feat. This means our new ability will
be called `Expert Defense` .

Note: You can have two abilities with the same name as long as they are
of different categories, i.e. the `CATEGORY` tag specifies a different
category for each ability.

**Example:**

`Expert Defense`

Amazingly enough, our new ability has the same name as our old feat.

------------------------------------------------------------------------

#### `CATEGORY:My Super Ability`

This tag identifies the 'category' in which your new ability will be
placed. In the case of our example ability, we are placing it in the
<span class="lstobj"> My Super Ability </span> category. Any category,
besides 'FEAT', must have been defined in the <span class="lstfile">
miscinfo.lst </span> or <span class="lstfile"> abilitycategory.lst
</span> file to be valid. See "The Ability Category File" file below.

Note: While ability categories can be named whatever you decide upon,
when using the hardcoded <span class="lstobj"> FEAT </span> category,
you must use all caps as that is the way it is hardcoded within PCGen.

------------------------------------------------------------------------

#### Our New Ability

All other tags in our example feat are used as is in our new ability.
The final Ability object is shown below:

`Expert Defense`

`CATEGORY:My Super Ability`

`TYPE:Special`

`VISIBLE:NO`

`SAB:Expert Defense ~ Add % bonus to AC|INT`

`BONUS:COMBAT|AC|INT`

------------------------------------------------------------------------

### The Ability Category File

The <span class="lstfile"> my\_abilitycategories.lst </span> file
defines the various ability categories that an ability can be assigned
to. These categories will determine where, within the PCGen user
interface, the related abilities will appear. In general, they will
appear in a sub-tab on the "Feats & Abilities" tag.

There are a number of ability categories built into PCGen's various
datasets, all defined in either the loaded gamemode's <span
class="lstfile"> miscinfo.lst </span> file or the loaded dataset's <span
class="lstfile"> abilitycategory.lst </span> file. For Homebrews, you'll
need to either use one of these existing ability categories or set up
your own "Ability Category", which in turn will create a separate "pool"
with which to manage your converted abilities. To demonstrate how this
is done, we'll use the <span class="lstobj"> My Super Ability </span>
category.

------------------------------------------------------------------------

#### `ABILITYCATEGORY:My Super Ability`

The first entry in the ABILITYCATEGORY line is the name of the new
ability category which identifies the "ABILITYPOOL". This ability pool
governs how many abilities can be taken, if they cost anything at all.
The "ABILITYCATEGORY" tag is not strictly required as PCGen will take
the first data entry as the name of the ability category, and thus the
ability pool, but current PCGen standard practice is to include the tag.

If this ability category is defined as "visible" (See the "VISIBLE" tag
below), any ability given this category will appear in the "Feats &
Abilities" tab under a sub-tab of the same name as this ability
category. In this case, <span class="lstobj"> My Super Ability </span> .

------------------------------------------------------------------------

#### `CATEGORY:Special Ability`

This is a 'super-category', or parent, to which our new ability category
belongs. This tag is optional but if included must list an existing
ability category that has been defined in either the <span
class="lstfile"> miscinfo.lst </span> file, an already loaded <span
class="lstfile"> abilitycategory.lst </span> file, or your new <span
class="lstfile"> abilitycategory.lst </span> file.

------------------------------------------------------------------------

#### `TYPE:Special`

This is a **TYPE** , or list of types, assigned to abilities of this
catgory. While some types do not have an effect other than allowing
additional filtering in the GUI, as is the case with the type <span
class="lstobj"> Special </span> , there are a number of standard ability
types used within PCGen that effect PCGen in different ways. <span
class="lstobj"> SpecialQuality </span> and <span class="lstobj">
SpecialAttack </span> are used to determine where on the Output Sheet
the associated abilities will be placed. <span class="lstobj">
FavoredEnemy </span> , <span class="lstobj"> RogueAbilities </span> ,
and <span class="lstobj"> General </span> effect which sub-tab the
associated abilities will appear on in the PCGen GUI.

A complete list of standard feat and ability types can be found on the
[Global TYPE](/list/global/type.html#feat) page.

------------------------------------------------------------------------

#### `PLURAL:My Super Abilities`

This has to do with the internationalization. An example is: `in_feats`
which sets the category key to 'in\_feats'. It also shows up with the
'Plural' of the name. An example of this is `Feat` would be `Feats` .
(Feats would display in the drop down bar).

------------------------------------------------------------------------

#### `EDITABLE:NO`

This defines whether a user can modify the abilities in the category.
**NO** would be appropriate for class abilities which aren't chosen by
the user.

------------------------------------------------------------------------

#### `EDITPOOL:NO`

This defines whether a user can modify the pool number or not. Generally
each ability has a 'cost' with a default cost of 1. If this option is
set to **NO** the user cannot manually add or subtract from the pool.
For feats, the default is **YES** .

------------------------------------------------------------------------

#### `FRACTIONALPOOL:NO`

This defines whether the pool must be a whole number or can be
fractions. Some abilities may have a cost less than '1' like .5 or .25.
Available options are `YES` or `NO` .

------------------------------------------------------------------------

#### `POOL:0`

This tag establishes the base ability pool for the defined ability
category. It will take a number, formula, or variable. If a variable is
used, the variable **MUST** be defined by a `DEFINE` tag. For our new
ability category, we will start with an ability pool of zero (0).

------------------------------------------------------------------------

#### `VISIBLE:NO`

Defines whether this category is visible on the UI or it it is hidden.
This tag is useful for hidden abilities and class abilities that require
no interaction from the user. Available options are - `YES` , `NO` , or
`QUALIFY` .

------------------------------------------------------------------------

#### `DISPLAYLOCATION`

The `DISPLAYLOCATION` is optional but will identify the sub-tab upon
which the associated abilities will be displayed. Examples of some
standard locations defined in the RSRD data set are "Class Abilities"
and "Special Qualities and Attacks". If it is not included the `PLURAL`
text will be used instead.

We will not be including this tag in our example ability category so you
can look for our converted abilities under the "My Special Abilities"
sub-tab.

Well, you could if we had not included the `VISIBLE:NO` tag in our
ability category entry.

------------------------------------------------------------------------

#### Our New Ability Category

The new entry in <span class="lstfile"> my\_abilitycategories.lst
</span> is shown below:

`ABILITYCATEGORY:My Super Ability`

`CATEGORY:Special Ability`

`PLURAL:My Super Abilities`

`EDITABLE:NO`

`EDITPOOL:NO`

`FRACTIONALPOOL:NO`

`POOL:0`

`VISIBLE:NO`

------------------------------------------------------------------------

### The PCC File

PCGen will use our <span class="lstfile"> my\_campaign.pcc </span> file
to identify which source files to load as well as other information
about the 'campaign'. Without these files and the related information,
PCGen would not be able to load any datafiles. For the purposes of this
lesson, there are only two tags we need to cover: The
`ABILITY:my_abilities.lst` tag and the
`ABILITYCATEGORY:my_abilitycategories.lst` tag.

PCGen will look in the <span class="lstfile"> my\_abilities.lst </span>
file for our newly converted abilities and in <span class="lstfile">
my\_abilitycategories.lst </span> file for any new ability categories
required to define the new abilities. These file references are relative
to the PCC file itself so if you provide no specific path beyond the
file names, PCGen will look in the same directory in which the pcc file
is contained.

There are three ways to call a file from an absolute location within the
PCGen installation. These are:

1.  The "at" symbol (@) will load the file from a path relative to the
    data folder. (Example:
    `ABILITY:@/d20ogl/srd35/basics/rsrd_abilities_class.lst` )
2.  The ampersand (&) will load the file from a path relative to the
    vendor data folder. (Example:
    `ABILITY:&/complete_monkey/complete_monkey_abilities.lst` )
3.  The asterisk (\*) will load the file from a path relative to the
    vendor data folder and if that does not exist, uses a path relative
    to the data folder. (Example:
    `ABILITYCATEGORY:*/d20ogl/srd35/basics/rsrd_ability_categories_core.lst` )

More information about PCC files can be found in the [PCC LST File
Class](/list/lst-file-class/01-pcc.html) .

------------------------------------------------------------------------

Final Thoughts
--------------

Unless you've made a new Ability Category, all feats converted to
abilities will show up on the 'Feats' tab as normal. Great examples of
new ability categories can be seen in the RSRD/SRD for the <span
class="lstobj"> Fighter </span> , <span class="lstobj"> Wizard </span>
and <span class="lstobj"> Rogue </span> class.

Remember, <span class="lstfile"> miscinfo.lst </span> is a gamemode
file, to define new ability categories or subcategories you MUST create
it there. There are entries about them in the docs if you want to read
up on them. To call the ability file it's (as you guessed),
`ABILITY:ability.lst` , in the .pcc file. Basically pretend that an
<span class="lstfile"> ability.lst </span> is a feat file as far as what
tags you can use in it and you'll be ok (fair warning though, there may
be exceptions to that rule of thumb).

You may continue to use [PREFEAT](/list/global/pre/prefeat.html) when
testing for the converted abilities as a prerequisite, as long as you
use the `CATEGORY:FEAT` tag, but it is recommended that you use
[PREABILITY](/list/global/pre/preability.html) instead. If you use any
other category, e.g. `CATEGORY:MySpecialAbility` , you **MUST** use the
`PREABILITY` tag to check for your new abilities as prerequisites.

Andrew\
 LST Chimp

------------------------------------------------------------------------



