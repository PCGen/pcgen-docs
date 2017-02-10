+++
date = "2016-08-01"
title = "KNOWNSPELLS (Data: classes.lst)"
original_url = "/list/data/classes.html#knownspells"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "KNOWNSPELLS"
    parent = "data_classes"
+++

## Status

None

## Syntax

`KNOWNSPELLS:x,x|x,x`

## Parameters

-   x: Text (Spell name)
-   x: TYPE=text (Spell type)
-   x: LEVEL=Number (Spell level)
-   x: .CLEARALL



<span id="knownspells"></span> \*\*\* Updated 5.11.4

What it does
------------

-   Provides a pipe-delimited (|) and comma-delimited list of spells, by
    name, level, or type that are automatically added to the
    spell caster.
-   Parameters included as a comma-delimited set must all be met by the
    spell for it to be granted to the spell caster.
-   Spells are granted only if the spell caster meets all prerequisites.
    (e.g. class level and required spell-stat score.)
-   `.CLEARALL` will clear all spells awarded on Class or Class Level
    line 0.
-   NOTE: Level 0 Class Level Line acts as a Class Level Line, otherwise
    Class Level Lines are NOT allowed.

Example
-------

`CLASS:Monkey Mage <tab> KNOWNSPELLS:Acid Fog`

The class knows the spell "Acid Fog" at 6th Level.

`CLASS:Monkey Mage <tab> KNOWNSPELLS:Acid Fog|Alarm`

The class knows the spell "Acid Fog" at 6th Level; and "Alarm" at 1st
Level.

`CLASS:Monkey Mage <tab> KNOWNSPELLS:LEVEL=3`

The class knows all level 3 spells available.

`CLASS:Monkey Cleric <tab> KNOWNSPELLS:TYPE=Divine`

The class knows all available divine spells.

`CLASS:Monkey Mage <tab> KNOWNSPELLS:LEVEL=3,TYPE=Arcane`

The class Monkey Mage knows all level 3 arcane spells available.

Where it is used
----------------

Class Line Only.

