+++
date = "2016-08-01"
title = "SPELLTYPE (Data: classes.lst)"
original_url = "/list/data/classes.html#spelltype"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "SPELLTYPE (Data: classes.lst)"
    parent = "classes"
+++

## Status

Deprecated 6.05.1 - use FACT

## Syntax

`SPELLTYPE:x`

## Parameters

-   x: Text (Spell type)



What it does
------------

The type of spells the character casts

Example
-------

`SPELLTYPE:Arcane`

The class uses arcane spells.

`CLASS:Defender.MOD <tab> SPELLSTAT:INT <tab> BONUSSPELLSTAT:NONE <tab> SPELLTYPE:Arcane <tab> SPELLBOOK:NO <tab> BONUS:CASTERLEVEL|Defender|TL <tab> SPELLLIST:1|Channeler`

Modifying the class Defender changes all of these tags to determine
bonus spells and maximum casting level.

Where it is used
----------------

Class Line.

