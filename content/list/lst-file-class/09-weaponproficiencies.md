+++
date = "2016-08-01"
title = "Lesson #9: .lst - Weapon Proficiencies"
original_url = "/list/lst-file-class/09-weaponproficiencies.html"

[menu.main]
    identifier = "lst-file-class_09-weaponproficiencies"
    name = "Lesson #9: .lst - Weapon Proficiencies"
    parent = "lst-file-class"
    
+++
By Professor Chris Chandler (Barak).

**File(s) Covered:** \*weaponprof.lst

**Tags used:**

`      TYPE          ,           HANDS          ,           IFLARGERTHANWEAPON          .`

The weapon proficiency files are used to set up weapon proficiency names
and the associated TYPES of weapons that they go with.

There is not that much to them so we'll dive right in.

------------------------------------------------------------------------

Weapon proficiency name

The weapon proficiency file is currently a lst file that has one weapon
proficiency entry per line. The first thing on each line is the name of
the weapon proficiency. There is no tag for it, the program assumes that
whatever is there at the beginning of the line is the name of a weapon
proficiency.

------------------------------------------------------------------------

**`TYPE`**

The TYPE tag is used to set the type/group of the weapon proficiency.
This defines for PCGen what type of weapon proficiency it takes for
characters to be able to use the weapon. It may take multiple types
delimited by periods, (although this is seldom done). The types used are
usually Simple, Martial, Exotic or Natural (and are defined in the game
mode files).

An example would be TYPE:Martial or TYPE.Exotic. If you wanted to get
more specific you could do TYPE:Martial.Sword.

It is important to note that this is the TYPE line that is searched when
you use a BONUS:WEAPONPROF=TYPE.yyyy tag. It grants a bonus to a weapon
whose associated \*weaponprof\* has the listed TYPE.

------------------------------------------------------------------------

**`HANDS`**

The HANDS tag sets the minimum number of hands required to use a weapon.
This tag is optional. If it is not present, the default value assumed by
PCGen is 1. While 1 and 2 are the standard entries, it would be possible
to craft a weapon/weapon proficiency for a creature that had three hands
and required all three to wield it properly.

`HANDS:1` and `HANDS:2` are examples of the use of this tag.

In addition, there is a flag that you may use in this tag that changes
it's behavior slightly. That flag is the IFLARGERTHANWEAPON flag,
described below

------------------------------------------------------------------------

**`IFLARGERTHANWEAPON`**

This is a flag to be used in conjunction with the hands tag. It
basically acts as a yes/no switch. If you append this to the HANDS
entry, PCGen will compare the size of the PC to the size of the weapon,
and grant the proficiency if the pc size is larger than the weapon size,
otherwise it will not apply.

This is used for certain weapons that are considered to be exotic
proficiencies if used with one hand, but martial if used with both
hands. Following is an example of this type of use (putting all of the
above information together for you as well):

> \
> `Bastard Sword (Exotic) TYPE:Exotic HANDS:1IFLARGERTHANWEAPON            Bastard Sword (Martial) TYPE:Martial HANDS:2`

That covers the weaponprof.lst files!

Barak\
 LST Chimp



