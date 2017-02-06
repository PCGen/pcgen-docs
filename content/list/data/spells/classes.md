+++
date = "2016-08-01"
title = "CLASSES (Data: spells.lst)"
original_url = "/list/data/spells.html#classes"
categories = [ "all-tag", "spells-tag" ]
[menu.main]
    name = "CLASSES (Data: spells.lst)"
    parent = "spells"
+++

## Status

Updated 5.11.11

## Syntax

`CLASSES:x,x=y|x,x=y`

## Parameters

-   x: Text (Class name)
-   x: ALL (All classes)
-   x: TYPE.Text (Class type)
-   x: .CLEARALL
-   y: Number (Spell level)



What it does
------------

-   This indicates that this spell is the indicated level for the
    named class.
-   Sub-classes may be listed as part of this tag but **MUST** also be
    included in a `SPELLLIST` tag in the appropriate class file object.
    For example, if the "Enchanter" subclass is included as part of a
    `CLASSES` tag in a spell, there must be an "Enchanter" subclass
    defined in a loaded class file.
-   `.CLEARALL` will clear all classes or class/level pairs from the
    `CLASSES` tag.
-   This tag can be qualified with PRExxx statements but all such PRExxx
    statements must be enclosed within square-brackets (\[\]) instead of
    the usual pipe-delineation (|).

Examples
--------

`CLASSES:Wizard=5|Enchanter=3|Druid=6`

Indicates this spell is 5th Lvl Wizard, 3rd Lvl Enchanter, and 6th Lvl
Druid.

`CLASSES:Wizard,Sorcerer=5|Cleric=4`

Indicates this spell is 5th Lvl Wizard, 5th Lvl Sorcerer, and 4th Lvl
Cleric.

`CLASSES:ALL=4`

Indicates this spell is 4th Lvl for all classes.

`CLASSES:TYPE.Divine=3`

Indicates this spell is 3rd Lvl for divine classes.

`CLASSES:ALL=4[PREDEITY:Java]`

Indicates this spell is 4th Lvl for all classes, but is only available
for followers of Java.

`CLASSES:Wizard,Sorcerer=5|Cleric=4[PRECLASS:1,Magician=1]`

Indicates this spell is 5th Lvl Wizard, 5th Lvl Sorcerer, but will only
be added to the spell list of a character with one level of the Magician
prestige class. This is especially useful if you need to create spell
lists for prestige classes that add caster levels to existing levels but
do not otherwise have a spell progression.

`Misdirection.MOD <tab> CLASSES:Circle Walker=2`

Indicates this spell is modified to 2nd Level for Circle Walker classes.

**.MOD Example (Appending):**

Initial Spell: `<spell name> <tab> CLASSES:Wizard=4`

Modified By: `<spell name>.MOD <tab> CLASSES:Cleris=3`

Is Equivalent To: `<spell name> <tab> CLASSES:Wizard=4|Cleric=3`

The associated spell is a 4th level Wizard spell and a 3rd level Cleric
spell.

