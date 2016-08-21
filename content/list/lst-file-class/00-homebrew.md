+++
date = "2016-08-01"
title = "Lesson #00: Building a Homebrew Data Set"
original_url = "/list/lst-file-class/00-homebrew.html"

[menu.main]
    identifier = "lst-file-class_00-homebrew"
    name = "Lesson #00: Building a Homebrew Data Set"
    parent = "lst-file-class"
    
+++
By Eric C. Smith (Maredudd)

------------------------------------------------------------------------

### LST File Class Overview

This LST File class will briefly cover how to build a homebrew data set
using the **my\_homebrew** template provided by the PCGen team.

**File Covered** : my\_homebrew files

[my\_campaign.pcc](/list/lst-file-class/00-homebrew.html#pcc)

[my\_abilities.lst](/list/lst-file-class/00-homebrew.html#ability)\
[my\_ability\_categories.lst](/list/lst-file-class/00-homebrew.html#abilitycategory)\
[my\_armorprofs.lst](/list/lst-file-class/00-homebrew.html#armorprof)\
[my\_classes.lst](/list/lst-file-class/00-homebrew.html#class)\
[my\_companionmods.lst](/list/lst-file-class/00-homebrew.html#companionmod)\

[my\_deities.lst](/list/lst-file-class/00-homebrew.html#deity)\
[my\_domains.lst](/list/lst-file-class/00-homebrew.html#domain)\
[my\_equipment.lst](/list/lst-file-class/00-homebrew.html#equipment)\
[my\_equipmods.lst](/list/lst-file-class/00-homebrew.html#equipmod)\
[my\_races.lst](/list/lst-file-class/00-homebrew.html#race)\

[my\_feats.lst](/list/lst-file-class/00-homebrew.html#feat)\
[my\_kits.lst](/list/lst-file-class/00-homebrew.html#kit)\
[my\_languages.lst](/list/lst-file-class/00-homebrew.html#language)\
[my\_races.lst](/list/lst-file-class/00-homebrew.html#race)\
[my\_shieldprofs.lst](/list/lst-file-class/00-homebrew.html#shieldprof)\

[my\_skills.lst](/list/lst-file-class/00-homebrew.html#skill)\
[my\_spells.lst](/list/lst-file-class/00-homebrew.html#spell)\
[my\_templates.lst](/list/lst-file-class/00-homebrew.html#template)\
[my\_weaponprofs.lst](/list/lst-file-class/00-homebrew.html#weaponprof)

------------------------------------------------------------------------

### Reading Conventions

A quick note on a few general conventions used within this class before
we jump into it:

1\) Throughout this lesson the angle brackets (&lt;&gt;) are used to
indicate where your text will be entered when building a data file.
Unless explicitly stated in the text, you will not include the angle
brackets in your tags.

2\) Coding examples and PCGen tags are identified by `<code>` style.

3\) Files referenced in this lesson are identified by <span
class="lstfile"> file.lst </span> style.

4\) When referencing a specific PCGen object, i.e. deity, feat, weapon,
etc., the object name will be formated as <span class="lstobj"> BOLD
</span> text, except for when the object is part of a `<code>` example.

------------------------------------------------------------------------

### Data Set Creation Overview

All PCGen data sets are made up of a collection of text files called LST
files, each of which contains a particular type of LST Object, e.g.
Class, Deity, Feat, Race, etc. For the new LST monkey this can be
confusing so the PCGen team has provided a basic template for a data
set. This template can be found in PCGen's *data/&lt;gamemode - 35e or
pathfinder&gt;/my\_homebrew* folder. In this LST Class we will provide
an introduction to the **my\_homebrew** data set template and get you
started building your own data set, whether it's for your own homebrewed
campaign or a simple addition or modification of an existing one to
incorporate house rules.

You will find below a short introduction to the data set template
itself, followed by a section that will cover each of the files which
can be found in the data set, covering each of the files listed below:

------------------------------------------------------------------------

### Introduction to the my\_homebrew Files

The <span class="lstfile"> my\_homebrew </span> template forms a
framework for building a dataset for use with PCGen. It is meant to be
used by beginners who want to take their first steps in entering their
own custom data into PCGen and have found that the built-in List Editors
are too limiting. The template consists of a collection of LST files,
one each for the different LST objects possible in PCGen. Copy these
files into your own folder to make your dataset, leaving the original
<span class="lstfile"> my\_homebrew </span> files as a clean template
for future use. You can rename the copied files to anything you wish but
it is generally a good idea to use some part of the name for the RPG
source material you plan on encoding. Also it is a good idea to retain
the type of LST object contained in the file as part of the file names.
An example of this might be <span class="lstfile"> rsrd\_feat.lst
</span> for the file containing the feats for WotC's Revised Standard
Reference Document (gamemode 35e). For the purposes of this class though
we will continue using the standard <span class="lstfile">
my\_homebrew.lst </span> naming convention. To use this template you
will find the LST file corresponding to the kind of LST object you wish
to create, i.e. <span class="lstfile"> my\_classes.lst </span> if you
want to add a new class, and enter your new data there. Each LST file
includes an example to give you a feel for what an entry in that
particular type of file would look like.

You will find below more information about each LST file, and the LST
objects that are defined in them, but you will also need to become
familiar with PCGen's included documentation. You will find this
documentation by starting PCGen and clicking on "Documentation" in the
Help menu. That will bring up a browser window in which you will find in
the navigation bar on the left a link to the 'List Files'. Clicking this
link will open a menu tree that includes the option 'LST File Tag Index'
which points to PCGen LST Tag Dictionary. You will also see a 'List File
Class' links that take you to the same classes linked to below. Nnot all
LST object types are covered by a LST File Class, but those that are
covered are covered well. For the rest, you can stop by
[ListFileHelp@Yahoo!](http://tech.groups.yahoo.com/group/PCGenListFileHelp/)
to get help.

Once you have created or editing your LST file you will need to edit the
<span class="lstfile"> my\_campaign.pcc </span> file. For every one of
the LST files included, you must set up a line that calls it inside of
the campaign file, but is commented out by use of a '\#' character.
Remove the '\#' from the beginning of the corresponding line. You might
also want to change the game mode, as it is now set to '35e', if your
custom data is meant for a different game mode.

You may also note a file called <span class="lstfile"> OGL.txt </span> ,
which we always need to distribute with data that is coming from an Open
Game Content Source. It is here because the examples in the \*.lst files
were mostly drawn from our dataset for the 3.5 System Reference
Document. It is not needed for your dataset to function.

If you use this framework to set up a dataset of your own, then you may
want to rename the folder and files to something different. Otherwise if
you ever should install a newer version of PCGen into your existing
directory or needed to re-install your existing installation of PCGen,
your changes would get overwritten and thus be lost.

------------------------------------------------------------------------

### <span id="pcc"></span> The PCGen Campaign Configuration (PCC) File

The PCC file is the most important file in a data set as it is the file
that PCGen uses to identify what data sets are available. Without the
PCC file, no data set would be loaded, so it is important when building
a homebrew data set that we start with the PCC file. Beyond identifying
the data set as a loadable set, the file also provides PCGen with
information on the campaign itself as well as the specific LST files to
be loaded.

For more information on building a PCC file see [LST File Class \#1: The
PCC - Campaign Information](/list/lst-file-class/01-pcc.html) and [LST
File Class \#2: The PCC - Basic File
Types](/list/lst-file-class/02-pcc.html) .

------------------------------------------------------------------------

### <span id="ability"></span> The Ability File

This section TBD.

For more information on converting Feats to Abilities see [LST File
Class \#17: Feats to Abilities, The Basic
Conversion](/list/lst-file-class/17-converting-feats-to-abilities.html)
.

------------------------------------------------------------------------

### <span id="abilitycategory"></span> The Ability Category File

This section TBD.

------------------------------------------------------------------------

### <span id="armorprof"></span> The Armor Proficiency File

This section TBD.

------------------------------------------------------------------------

### <span id="class"></span> The Class File

This section TBD.

------------------------------------------------------------------------

### <span id="companionmod"></span> The Companion Modification File

This section TBD.

------------------------------------------------------------------------

### <span id="deity"></span> The Deity File

This section TBD.

For more information on building a Deity file see [LST File Class \#14:
Deities](/list/lst-file-class/14-deities.html) .

------------------------------------------------------------------------

### <span id="domain"></span> The Domain File

This section TBD.

For more information on building a Domain file see [LST File Class \#15:
Domain Basics](/list/lst-file-class/15-domains-1.html) and [LST File
Class \#16: Domain Advanced
Topics](/list/lst-file-class/16-domains-2.html) .

------------------------------------------------------------------------

### <span id="equipment"></span> The Equipment File

This section TBD.

------------------------------------------------------------------------

### <span id="eqmod"></span> The Equipment Modification File

This section TBD.

------------------------------------------------------------------------

### <span id="feat"></span> The Feat File

This section TBD.

For more information on building a Feat file see [LST File Class \#2:
Feat Basics](/list/lst-file-class/12-feat-1.html) and [LST File Class
\#13: Feat Prereqs](/list/lst-file-class/13-feat-2.html) .

------------------------------------------------------------------------

### <span id="language"></span> The Language File

This section TBD.

For more information on building a Language file see [LST File Class
\#10: Languages](/list/lst-file-class/10-languages.html) .

------------------------------------------------------------------------

### <span id="race"></span> The Race File

This section TBD.

For more information on building a Feat file see [LST File Class \#3:
Races 1](/list/lst-file-class/03-race-1.html) , [LST File Class \#4:
Race 2](/list/lst-file-class/04-race-2.html) , [LST File Class \#2: Race
3](/list/lst-file-class/05-race-3.html) , and [LST File Class \#4: Race
4](/list/lst-file-class/06-race-4.html) .

------------------------------------------------------------------------

### <span id="shieldproficiency"></span> The Shield Proficiency File

This section TBD.

------------------------------------------------------------------------

### <span id="skill"></span> The Skill File

This section TBD.

------------------------------------------------------------------------

### <span id="spell"></span> The Spell File

This section TBD.

For more information on building a Spell file see [LST File Class \#07:
Spells](/list/lst-file-class/07-spells.html) .

------------------------------------------------------------------------

### <span id="kit"></span> The Starting Kit File

This section TBD.

For more information on building a Starting Kit file see [LST File Class
\#11: Default Monster
Kits](/list/lst-file-class/11-kits-default-monster.html) .

------------------------------------------------------------------------

### <span id="template"></span> The Template File

This section TBD.

------------------------------------------------------------------------

### <span id="weaponproficiency"></span> The Weapon Proficiency File

This section TBD.

For more information on building a Weapon Proficiency file see [LST File
Class \#09:
Weaponprofs](/list/lst-file-class/09-weaponproficiencies.html) .

------------------------------------------------------------------------

You should now have at least a basic understanding of how a homebrew
data set should be organized. Take a look at the LST File Classes linked
to in this article for more detail.

Maredudd

------------------------------------------------------------------------



