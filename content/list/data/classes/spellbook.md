+++
date = "2016-08-01"
title = "SPELLBOOK (Data: classes.lst)"
original_url = "/list/data/classes.html#spellbook"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "SPELLBOOK"
    parent = "data_classes"
    identifier = "data_classes_SPELLBOOK"
+++

## Status

None

## Syntax

`SPELLBOOK:x`

## Parameters

-   Variables Used: YES or NO



What it does
------------

Means that the class is required to use a spellbook as a wizard does.

Example
-------

`SPELLBOOK:YES`

The class uses a spellbook.

`CLASS:Defender.MOD <tab> SPELLSTAT:INT <tab> BONUSSPELLSTAT:NONE <tab> SPELLTYPE:Arcane <tab> SPELLBOOK:NO <tab> BONUS:CASTERLEVEL|Defender|TL <tab> SPELLLIST:1|Channeler`

Modifying the class Defender changes all of these tags to determine
bonus spells and maximum casting level.

Where it is used
----------------

Class Level Line.

**Default Value:**

`NO`

