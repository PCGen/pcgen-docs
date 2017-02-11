+++
date = "2016-08-01"
title = "SPELLKNOWN (Global: OTHER)"
original_url = "/list/global/other.html#spellknown"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "SPELLKNOWN"
    parent = "global_other"
    identifier = "global_other_SPELLKNOWN"
+++

## Status

Updated 6.00.x

## Syntax

`SPELLKNOWN:CLASS|w=x|y|w=x|y|z|z`

## Parameters

-   w: Text (Class Name)
-   w: SPELLCASTER.Text (Spellcaster Type)
-   x: Number (Spell Level)
-   y: Text (Spell List)
-   z: PRExxx tag



What it does
------------

-   This tag adds spells to the character's list of known spells.
-   The spell list (y) is a comma-delimited list of spell names.

Examples
--------

`SPELLKNOWN:CLASS|Arawnite Guardian=0|Create Water,Detect Magical Aura,Light,Mending,Read Magic,Resistance,Virtue`

This is the character's known spell's for the Arawnite Guardian class.

`1 <tab> SPELLKNOWN:CLASS|Trundlefolk Shaman=0|Create Water,Cure Minor Wounds,Detect Magic,Guidance,Mending,Purify Food and Drink`

This is the character's known spell's for the first level Trundlefolk
Shaman class.

`SPELLKNOWN:CLASS|SPELLCASTER.Psionic=7|Hypercognition`

The Hypercognition power is added to the character's Psionic
spallcasting classes.

`SUBCLASSLEVEL:1 <tab> SPELLKNOWN:CLASS|Holy Warrior=1|Bless,Bless Water,Bless Weapon,Create Water,Cure Light Wounds,Detect Poison,Detect Undead,Divine Favor,Endure Elements,Magic Weapon,Protection from Evil,Read Magic,Resistance,Virtue`

This is the character's known spell's for the first level Holy Warrior
subclass.

