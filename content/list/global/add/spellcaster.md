+++
date = "2016-08-01"
title = "SPELLCASTER (Global: ADD)"
original_url = "list/global/add.html#spellcaster"
categories = [ "all-tag", "add-tag" ]
+++

## Status

New 5.11.11

## Syntax

`ADD:SPELLCASTER|x|y,y`

## Parameters

-   x: Number, Variable or Formula (Number of
    choices granted. Optional)
-   y: Text (Class name)
-   y: Text (Spellcasting class type, i.e. Arcane,
    Divine, Psionic)
-   y: ANY



What it does
------------

-   This grants a single bonus level to the spell casting class chosen.
-   When allowing more than one selection, including a count (x) of
    greater than one, multiple classes can be selected but the same
    class cannot be selected twice.
-   If you wish to select the same class more than once, you must use
    two tags.
-   The bonus level confers only its spellcasting capabilities, no other
    bonuses or benefits from the class are granted.
-   When used on a class line the list of choices that come up will NOT
    include the class that the tag is in.
-   The specified class must have its own spell list.
-   This tag will not grant a bonus spell casting level for a class that
    uses the CASTAS tag or in some other way rides on another class's
    spell list.
-   The "ANY" property will present a list of all the spellcasting
    classes the PC already has levels in.
-   When using a type such as Divine or Arcane the SPELLTYPE of all the
    spellcasting classes the PC has levels in are checked and those that
    match are presented.
-   When using specific class names those are the classes presented, the
    PC does NOT need to have any levels in those classes in order to
    select them.

Examples
--------

`ADD:SPELLCASTER|ANY`

Adds a bonus level of spellcasting to any spellcasting class the
character has levels in.

`ADD:SPELLCASTER|Divine`

Adds a bonus level of spellcasting to any Divine spellcasting class the
character has levels in.

`ADD:SPELLCASTER|Arcane`

Adds a bonus level of spellcasting to any Arcane spellcasting class the
character has levels in.

`ADD:SPELLCASTER|Bard,Sorcerer`

Adds a bonus level of spellcasting of either Bard or Sorcerer.

