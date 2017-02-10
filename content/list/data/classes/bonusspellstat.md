+++
date = "2016-08-01"
title = "BONUSSPELLSTAT (Data: classes.lst)"
original_url = "/list/data/classes.html#bonusspellstat"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "BONUSSPELLSTAT"
    parent = "data_classes"
    identifier = "data_classes_BONUSSPELLSTAT"
+++

## Status

None

## Syntax

`BONUSSPELLSTAT:x`

## Parameters

-   x: Text (Abbreviated name of stat from
    statsandchecks.lst or "None")



<span id="bonusspellstat"></span> \*\*\* Added 4.3.1

What it does
------------

-   Changes the Stat used to determine Bonus spells that a spell caster
    get from high ability score from the SPELLSTAT named Stat.
-   If not present, the SPELLSTAT will determine DCs and bonus spells.
-   If set to NONE no bonus spells will be granted.

Example
-------

`BONUSSPELLSTAT:STR`

The class uses Strength to determine bonus spells.

`CLASS:Defender.MOD <tab> SPELLSTAT:INT <tab> BONUSSPELLSTAT:NONE <tab> SPELLTYPE:Arcane <tab> SPELLBOOK:NO <tab> BONUS:CASTERLEVEL|Defender|TL <tab> SPELLLIST:1|Channeler`

Modifying the class Defender changes all of these tags to determine
bonus spells and maximum casting level.

Where it is used
----------------

Class Line.

