+++
date = "2016-08-01"
title = "HANDS (Data: weapon_proficiencies.lst)"
original_url = "list/data/weaponproficiencies.html#hands"
categories = [ "all-tag", "weaponproficiencies-tag" ]
+++

## Status

None

## Syntax

`HANDS:x`

## Parameters

-   x: Number (Number of hands)



p class="status"&gt; <span id="hands"></span> \*\*\* Updated

What it does
------------

-   Determines the minimum number of hands required to use the weapon.
    Defaults to a value of 1.
-   `#IFLARGERTHANWEAPON` is a flag that checks if the characters size
    is larger than the weapon.
    -   If true, the character is granted that prof.
    -   If not, the proficiency does not apply.
-   Used for Exotic 1-Hand weapons that are martial if wielded with
    both hands.
-   When modifying a weapon proficiency with the `.MOD` tag, given an
    existing `HANDS` tag, the data included in a new `HANDS` tag will
    overwrite the existing tag data.

Examples
--------

`HANDS:2`

Weapon is wielded with two hands.

`HANDS:1IFLARGERTHANWEAPON`

Weapon is wielded with one hand if the PC is larger than the weapon
size.

**.MOD Example:**

Initial Template: `Ogre Axe <tab> HANDS:1`

Modified By: `Ogre Axe.MOD <tab> HANDS:2`

Results In: `Ogre Axe <tab> HANDS:2`

Weapon is wielded with two hands.

