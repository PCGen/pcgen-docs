+++
date = "2016-08-01"
title = "SPELLSSPELLBOOK (Data: starting_kits.lst)"
original_url = "/list/data/startingkits.html#spellsspellbook"
categories = [ "all-tag", "startingkits-tag" ]
[menu.main]
    name = "SPELLSSPELLBOOK"
    parent = "data_startingkits"
    identifier = "data_startingkits_SPELLSSPELLBOOK"
+++

## Status

New 5.9.3

## Syntax

`SPELLS:SPELLBOOK=v|CLASS=w|x|x[y]=z`

## Parameters

-   v: Text (Spellbook name)
-   w: Text (Spellcasting class name)
-   x: Text (Spell name)
-   y: Text (Metamagic Feat name, optional)
-   z: Number (Number of time the spell appears in
    the book)



What it does
------------

-   Adds the named spell (x) to the spellbook (v) for the class (w).
-   \[y\] is any metamagic feat known to the character.

Examples
--------

`SPELLS:SPELLBOOK=Prepared Spells|CLASS=Cleric|Aid=3|Align Weapon|Banishment`

Would add Aid, Align Weapon and Banishment to the Prepared Spells
spellbook, Aid appears three times.

`SPELLS:SPELLBOOK=Known Spells|CLASS=Sorcerer|Daze|Detect Magic|Ghost Sound`

Adds Daze, Detect Magic and Ghost Sound to the Sorcerer's Known Spells
spellbook.

