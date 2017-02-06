+++
date = "2016-08-01"
title = "ABILITYCATEGORY (Data: ability_categories.lst)"
original_url = "/list/data/abilitycategory.html#abilitycategory"
categories = [ "all-tag", "abilitycategory-tag" ]
[menu.main]
    name = "ABILITYCATEGORY (Data: ability_categories.lst)"
    parent = "abilitycategory"
+++

## Status

None

## Syntax

`ABILITYCATEGORY:x`

## Parameters

-   x: Text (Name of the Ability Category).



\*\*\* Added 5.13.5

What it does
------------

-   The ABILITYCATEGORY tag begins a line which defines a category
    of abilities.
-   The ABILITYCATEGORY tag is optional as PCGen will take the first
    data element in each line as the name of the ability category
    being defined.
-   Visible ability categories will show as a sub-tab on the
    abilities tab.
-   If no extra parameters are provided on the line the category will
    default to being visible, editable, with no types, a display name
    and plural name matching the category name and an editable whole
    number only pool with a starting value of 0.

Example
-------

`ABILITYCATEGORY:Special Attack`

Defines a category named Special Attack.

`Special Attack <tab> PLURAL=Ambush`

Defines a category named Special Attack and sets the internationalized
name to "Ambush".

The following tags are used in ABILITYCATEGORY lines and are defined in
the
[*miscinfo.lst*](/list/system/gamemode-miscinfo/abilitycategory.html)
file documentation:

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
-   [POOL](/list/system/gamemode-miscinfo/pool.html) - Sets the number,
    variable, or formula used to calculate the pool size for this
    category of ability.
-   [TYPE](/list/system/gamemode-miscinfo/type.html) - Defines the list
    of types included in this category
-   [VISIBLE](/list/system/gamemode-miscinfo/visible.html) - Defines
    whether this category of ability should be displayed in the UI.


