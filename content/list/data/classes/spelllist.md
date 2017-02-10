+++
date = "2016-08-01"
title = "SPELLLIST (Data: classes.lst)"
original_url = "/list/data/classes.html#spelllist"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "SPELLLIST"
    parent = "data_classes"
+++

## Status

None

## Syntax

`SPELLLIST:x|y|y`

## Parameters

-   x: Number (number of choices)
-   y: Text (Class Name)
-   y: DOMAIN.Text (Domain Name)



<span id="spelllist"></span> \*\*\* Updated 5.11.4 \*\*\*

What it does
------------

-   This is an optional tag with PCGen defaulting to the class name as
    the name of the spell list if this tag is not included.
-   Following the number of choices (x), this is a pipe-delimited (|)
    list of class names (y) that the class can choose from to duplicate
    spell casting ability.
-   For a spellcasting class with subclasses that have separate spell
    lists, the `SPELLLIST` tag should be included in the subclass
    line only.

Example
-------

`CLASS:Faemancer <tab> SPELLLIST:1|Ranger`

The class uses the ranger spell list.

`SUBCLASS:Egoist <tab> SPELLLIST:1|Ranger|Druid`

The subclass uses either the ranger or druid spell list.

`CLASS:War Mind <tab> SPELLLIST:2|Ranger|Druid|Barabarian`

The class uses 2 of the ranger, Druid or Barbarian spell lists.

`CLASS:Blood Witch <tab> SPELLLIST:1|DOMAIN.Animal`

The class uses the Animal Domain spell list.

`CLASS:Rogue.COPY=Blood Witch <tab> SPELLLIST:1|DOMAIN.Animal`

Copy class Rogue to Blood Witch useing the Animal Domain spell list.

`CLASS:Defender.MOD <tab> SPELLSTAT:INT <tab> BONUSSPELLSTAT:NONE <tab> SPELLTYPE:Arcane <tab> SPELLBOOK:NO <tab> BONUS:CASTERLEVEL|Defender|TL <tab> SPELLLIST:1|Channeler`

Modifying the class Defender changes all of these tags to determine
bonus spells and maximum casting level.

Where it is used
----------------

Class Line, SubClass line or SubstitutionClass line.

