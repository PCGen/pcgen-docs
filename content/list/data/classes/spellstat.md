+++
date = "2016-08-01"
title = "SPELLSTAT (Data: classes.lst)"
original_url = "/list/data/classes.html#spellstat"
categories = [ "all-tag", "classes-tag" ]
[menu.main]
    name = "SPELLSTAT"
    parent = "data_classes"
+++

## Status

None

## Syntax

`SPELLSTAT:x`

## Parameters

-   x: Text (abbreviated name of stat
    from statsandchecks.lst)
-   x: SPELL
-   x: OTHER



What it does
------------

-   Used to tell PCGen what attribute/stat to use for determining bonus
    spells and maximum level the character can cast
-   Used in a Subclass Line this tag overwrites any `SPELLSTAT` tag in
    the main Class Line.
-   The stat specified can be any stat defined in <span class="lstfile">
    statsandchecks.lst </span> system file.
-   Use of the `SPELL` subtag tells PCGen to use the stat specified in
    the `SPELLSTAT` tag located in the class' individual spells.
-   Use of the `OTHER` subtag will result in no stat bonuses
    being granted.

Examples
--------

`SPELLSTAT:INT`

This class/subclass uses Intelligence to determine maximum level of
spells.

`SPELLSTAT:SPELL`

This class/subclass uses the stat specified in the `STAT:x` tag in the
spells the class/subclass uses.

`SPELLSTAT:OTHER`

Thia class/subclass does not recieve a stat bonus for spell casting.

`CLASS:Defender.MOD <tab> SPELLSTAT:INT <tab> BONUSSPELLSTAT:NONE <tab> SPELLTYPE:Arcane <tab> SPELLBOOK:NO <tab> BONUS:CASTERLEVEL|Defender|TL <tab> SPELLLIST:1|Channeler`

Modifies the **Defender** class's spell stat is changed to the
intelligence stat.

Where it is used
----------------

Class or Subclass Line.

