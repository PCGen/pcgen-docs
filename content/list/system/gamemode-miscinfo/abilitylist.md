+++
date = "2016-08-01"
title = "ABILITYLIST (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#abilitylist"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "ABILITYLIST"
    parent = "system_gamemode-miscinfo"
+++

## Status

New 5.15.10

## Syntax

`ABILITYLIST:x|x(y)`

## Parameters

-   x: Text (Ability Key).
-   y: Text (Ability Sub-Choices).



What it does
------------

-   Defines a list of abilities and their choices (aka sub keys) that
    are included in the associated category.
-   These abilities are in addition to the abilities included in the
    category by the TYPE tag.
-   When a subkey is specified for an ability, only the listed choices
    will be valid for that ability in the category.
-   This tag is valid only in "child" ability categpries. (See
    [CATEGORY](/list/system/gamemode-miscinfo/category.html) tag.)

Example
-------

`ABILITYLIST:Mounted Combat|Skill Focus (Ride)|Skill Focus (Handle Animal)|Ride-By Attack`

Defines that Mounted Combat, Ride-By Attack and Skill Focus should be
included in the category. However only Ride and Handle Animal will be
offered if Skill Focus is chosen from this category.

`ABILITYLIST:Weapon Finesse`

Defines that Weapon Finesse should be included in the category. As no
subkey is defined, the normal choices will be offered if Weapon Finesse
is chosen from this category.

Where it is Used
----------------

Used in
[ABILITYCATEGORY](/list/system/gamemode-miscinfo/abilitycategory.html)
lines.

