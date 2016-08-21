+++
date = "2016-08-01"
title = "SPELLLEVEL (Global: OTHER)"
original_url = "list/global/other.html#spelllevel"
categories = [ "all-tag", "other-tag" ]
+++

## Status

Updated 6.00.x

## Syntax

`SPELLLEVEL:v|w=x|y|w=x|y|z|z`

## Parameters

-   v: DOMAIN
-   v: CLASS
-   w: Text (Domain or Class Name)
-   w: SPELLCASTER.Text (Spellcaster Type)
-   x: Number (Spell Level)
-   y: Text (Spell List)
-   z: PRExxx tag



What it does
------------

-   This is the character's spell list.
-   The `SPELLCASTER` subtag is used only with the `CLASS` subtag.
-   The spell list (y) is a comma-delmited list of spell names.

Examples
--------

`SPELLLEVEL:DOMAIN|Cold=1|Endure Elements|Cold=2|Chill Metal|Cold=3|Sleet Storm|Cold=4|Wall of Ice|Cold=5|Cone of Cold|Cold=6|Freezing Sphere|Cold=7|Control Weather|Cold=8|Finger of Death|Cold=9|Elemental Swarm`

This is the character's spell's for the Cold domain.

`SPELLLEVEL:CLASS|Arawnite Guardian=0|Create Water,Detect Magical Aura,Light,Mending,Read Magic,Resistance,Virtue`

This is the character's spell's for the Arawnite Guardian class.

`SPELLLEVEL:CLASS|SPELLCASTER.Psionic=7|Hypercognition`

The Hypercognition power is added to the character's Psionic
spallcasting classes.

`1 <tab> SPELLLEVEL:CLASS|Trundlefolk Shaman=0|Create Water,Cure Minor Wounds,Detect Magic,Guidance,Mending,Purify Food and Drink`

This is the character's spell's for the first level Trundlefolk Shaman
class.

`SUBCLASSLEVEL:1 <tab> SPELLLEVEL:CLASS|Holy Warrior=1|Bless,Bless Water,Bless Weapon,Create Water,Cure Light Wounds,Detect Poison,Detect Undead,Divine Favor,Endure Elements,Magic Weapon,Protection from Evil,Read Magic,Resistance,Virtue`

This is the character's spell's for the first level subclass Holy
Warrior class.

`The Dead <tab> NAMEISPI:NO <tab> SPELLLEVEL:DOMAIN|The Dead=1|Detect Return|The Dead=2|Consecrate|The Dead=3|Negative Energy Protection|The Dead=4|Touch of Return|The Dead=5|Hallow|The Dead=6|Heal|The Dead=7|Greater Restoration|The Dead=8|Greater Return|The Dead=9|Imprison Soul`

This is the character's spell's for the Domain.

