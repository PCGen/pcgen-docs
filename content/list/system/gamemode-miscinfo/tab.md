+++
date = "2016-08-01"
title = "TAB (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#tab"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "TAB"
    parent = "system_gamemode-miscinfo"
+++

## Status

Updated 6.1.7

## Syntax

`TAB:x`

## Parameters

-   x: Text (Tab Name).



What it does
------------

-   This indicates what "TABS" will be displayed in the graphic user
    interface of the PCGen program.
-   Indicates which tab the options following it will affect. Must be
    first on the line, to be followed by
    [NAME](/list/system/gamemode-miscinfo/name.html) and
    [CONTEXT](/list/system/gamemode-miscinfo/context.html) (and
    optionally [VISIBLE](/list/system/gamemode-miscinfo/visible.html) ).
-   Tab Name may be one of:\
    -   CHARACTER SHEET - The tab showing a character sheet for
        the character.
    -   CLASS - The tab where classes are displayed.
    -   COMPANIONS - The tab where followers, familiars and animal
        companions are displayed.
    -   DESCRIPTION - The tab where character descriptive information
        is displayed.
    -   DOMAINS - The tab where deity/domain information is displayed.
    -   FEATS - The tab where feat information is displayed.
    -   INVENTORY - The tab where inventory and equipping are displayed.
    -   -   PURCHASE - The tab where a character owned gear
            is displayed.
        -   EQUIPPING - The tab where the loactions of the equipment
            are displayed.
    -   RACE - The tab where races are displayed.
    -   SKILLS - The tab where skills are displayed.
    -   SPELLS - The tab where spells are displayed.
    -   -   KNOWN - The tab where the spells the character knows
            are displayed.
        -   PREPARED - The tab where the spells the character has
            prepared are displayed.
        -   SPELLBOOKS - The tab where the spells the character has
            recorded in spellbooks are displayed.
    -   SUMMARY - The tab with summary information.
    -   TEMPLATES - The tab where templaes are displayed.
    -   TEMPMOD - The tab where temporary bonuses are displayed.

-   If the game mode doesn't support the TAB, you must use the
    Tag VISIBLE:NO.

Example
-------

`TAB:SUMMARY`

Indicates that the line will effect the "Summary" tab.

Where it is used
----------------

TAB Line.

