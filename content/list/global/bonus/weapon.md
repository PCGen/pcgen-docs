+++
date = "2016-08-01"
title = "WEAPON (Global: BONUS)"
original_url = "/list/global/bonus.html#weapon"
categories = [ "all-tag", "bonus-tag" ]
[menu.main]
    name = "WEAPON"
    parent = "global_bonus"
+++

## Status

Updated 5.14.0

## Syntax

`BONUS:WEAPON|x,x|y`

## Parameters

-   x: Property (Weapon property)
-   y: Number, Variable or Formula (Number to add)



What it Does
------------

-   Modifies the indicated property of the weapon the tag is
    contained in.
-   This tag only works in Equipment, Equipmod and temporary
    bonuses files.
-   PRE tags have no baring on how the tags they are appended to can be
    used, they only effect when they are applied.
-   Weapon properties defined are:
    -   `ATTACKS` - Adds a number of additional attacks.
    -   `ATTACKSPROGRESS` - Overrides the standard attack progression.
    -   `DAMAGE` - Adds to the damage of the weapon.
    -   `DAMAGEMULT` - Adds to the damage multiplier, See
        [BONUS:COMBAT|DAMAGEMULT](/list/global/bonus/combat.html)
        for syntax.
    -   `DAMAGESIZE` - Raises or lowers the damage dice on the same
        scale as weapon size, See
        [BONUS:COMBAT|DAMAGESIZE](/list/global/bonus/combat.html) for
        the scale.
    -   `DAMAGE-SHORTRANGE` - Adds to the damage of the weapon when used
        at short range.
    -   `TOHIT` - Adds to the attack bonus of the weapon.
    -   `TOHIT-SHORTRANGE` - Adds to the attack bonus of the weapon when
        used at short range.
    -   `WEAPONBAB` - Modifies the character's BAB for the weapon the
        bonus is applied to, affecting both to-hit and
        attack progression.
    -   `WIELDCATEGORY` - Raises or lowers the wieldcatagory of
        the weapon.

Examples
--------

`BONUS:WEAPON|DAMAGE|1`

Adds one to weapon damage.

`BONUS:WEAPON|DAMAGE-SHORTRANGE|1`

Adds one to short range weapon damage.

`BONUS:WEAPON|TOHIT|1`

Adds one to weapon to-hit.

`BONUS:WEAPON|TOHIT-SHORTRANGE|1`

Adds one to short range weapon to-hit.

`BONUS:WEAPON|TOHIT,DAMGE|1`

Adds one to weapon to-hit and damage.

`BONUS:WEAPON|ATTACKS|1`

Adds one attack to the weapon's attack progression.

`BONUS:WEAPON|ATTACKSPROGRESS|1`

Limits the weapon's attack progression to one.

`BONUS:WEAPON|WIELDCATEGORY|1`

Raises the weapon's wieldcatagory, if it were Light it becomes
OneHanded.

`BONUS:WEAPON|DAMAGE,TOHIT|min(2,(TL/6)|TYPE=Enhancement|PRELEVEL:6`

Raises the weapon's damage and to-hit, between 2 and (Total Level
divided by 6) if character is over level 6.

`BONUS:WEAPON|DAMAGEMULT:1|.5`

Increases the damage multiplier of the weapon by half your strength
bonus when wielded in your primary hand.

