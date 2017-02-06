+++
date = "2016-08-01"
title = "ABILITYCATEGORY (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#abilitycategory"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "ABILITYCATEGORY (Game Mode: miscinfo.lst)"
    parent = "gamemode-miscinfo"
+++

## Status

New 5.11.1

## Syntax

`ABILITYCATEGORY:x`

## Parameters

-   x: Text (Name of the Ability Category).



What it does
------------

-   ABILITYCATEGORY begins a line which defines a category of abilities.
-   Visible ability categories will show as a sub-tab on the
    abilities tab.
-   If no extra parameters are provided on the line the category will
    default to being visible, editable, with no types, a display name
    and plural name matching the category name and an editable whole
    number only pool with a starting value of 0.
-   Ability categories can also be defined as part of a source dataset,
    see the [ABILITYCATEGORY file](/list/data/abilitycategory.html)
    documentation for details.

The following tags are used in ABILITYCATEGORY lines:

-   [ABILITYLIST](/list/system/gamemode-miscinfo/abilitylist.html) -
    Defines a list of abilities that are included in the
    associated category.
-   [CATEGORY](/list/system/gamemode-miscinfo/category.html) - Defines
    the low-level ability category the category refers to.
    -   Class Abilities, Racial Abilities, Special Attacks, Special
        Qualities, Feat, Skill, Supernatural, Extraordinary and
        Spell, etc...
-   [DISPLAYLOCATION](/list/system/gamemode-miscinfo/displaylocation.html) -
    Define the name of the sub tab that the ability category will be
    displayed on.
-   [DISPLAYNAME](/list/system/gamemode-miscinfo/displayname.html) -
    Defines the display name of the category.
-   [EDITABLE](/list/system/gamemode-miscinfo/editable.html) - Defines
    whether this category of abilities is user-editable.
-   [EDITPOOL](/list/system/gamemode-miscinfo/editpool.html) - Sets the
    flag to allow/disallow user editing of the pool.
-   [FRACTIONALPOOL](/list/system/gamemode-miscinfo/fractionalpool.html) -
    Sets if the pool can use fractional amounts.
-   [PLURAL](/list/system/gamemode-miscinfo/plural.html) - Sets the
    internationalized plural name for this category.
-   [POOL](/list/system/gamemode-miscinfo/pool.html) - Sets the formula
    to use to calculate the base pool size for this category of ability.
-   [TYPE](/list/system/gamemode-miscinfo/type.html) - Defines the list
    of types included in this category
-   [VISIBLE](/list/system/gamemode-miscinfo/visible.html) - Defines
    whether this category of ability should be displayed in the UI.

Example
-------

`ABILITYCATEGORY:Special Attack`

Defines a category named Special Attack.

`ABILITYCATEGORY:Special Attack <tab> PLURAL=Ambush`

Defines a category named Special Attacka andsets the internationalized
name to "Ambush".

