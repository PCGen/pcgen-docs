+++
date = "2016-08-01"
title = "WEAPONPROF (Global: BONUS)"
original_url = "list/global/bonus.html#weaponprof"
categories = [ "all-tag", "bonus-tag" ]
+++

## Status

Updated 6.01.3

## Syntax

`BONUS:WEAPONPROF=x|y,y|z`

## Parameters

-   x: Text (Weapon proficiency name)
-   x: TYPE.Text (Weapon proficiency type)
-   y: Property (Weapon proficiency property)
-   z: Number, variable or formula (Number to add)



What it Does
------------

-   Modifies the indicated property of the weapon proficiency or weapon
    proficiency type.
-   Weapon proficiency properties defined are:
    -   `CRITMULTADD` adds to the critical multiplier of the weapon.
    -   `CRITRANGEADD` (adds to the critical range of the weapon.
    -   `CRITRANGEDOUBLE` doubles the critical range of the weapon.
    -   `DAMAGE` adds to the damage of the weapon.
    -   `DAMAGEMULT` adds to the damage multiplier, See
        [BONUS:COMBAT|DAMAGEMULT](/list/global/bonus/combat.html)
        for syntax.
    -   `DAMAGESIZE` raises or lowers the damage dice on the same scale
        as weapon size, See
        [BONUS:COMBAT|DAMAGESIZE](/list/global/bonus/combat.html) for
        the scale.
    -   `DAMAGE-SHORTRANGE` adds to the damage of the weapon at short
        range as defined in the GameMode files.
    -   `PCSIZE` adds to the character's size in relation to the weapon.
    -   `REACH` modifies the REACH for the specified weapon.
    -   `TOHIT` adds to the attack bonus of the weapon.
    -   `TOHIT-SHORTRANGE` adds to the attack bonus of the weapon at
        short range as defined in the GameMode files.
    -   `TOHITOVERSIZE` decreases the handedness of a weapon.
    -   `WEAPONBAB` - Modifies the character's BAB for the weapon
        proficiency the bonus is applied to, affecting both to-hit and
        attack progression.
    -   `WIELDCATEGORY` raises or lowers the wieldcatagory of
        the weapon.

Examples
--------

`BONUS:WEAPONPROF=Dagger|DAMAGE|1`

Adds one to dagger weapon damage.

`BONUS:WEAPONPROF=Dagger|DAMAGE,TOHIT|2`

Adds two to dagger weapon attack bonus and damage.

`BONUS:WEAPONPROF=TYPE.Martial|CRITRANGEADD|1`

Adds one to the critical range of any Martial type weapon.

`BONUS:WEAPONPROF=Shortbow|DAMAGE-SHORTRANGE|1`

Adds one to the damage of Shortbows at short range.

`BONUS:WEAPONPROF=Longsword|PCSIZE|1`

Allows a small character to use a longsword as if he were medium sized.

`BONUS:WEAPONPROF=Bite|REACH|5`

Would increase the reach of a creature's Bite by 5.

`BONUS:WEAPONPROF=Greatsword|TOHITOVERSIZE|1`

Allows a medium character to use a Greatsword one handed without
penalty.

`BONUS:WEAPONPROF=Longsword|WIELDCATEGORY|-1`

Lowers the weapon's wieldcatagory, if it were OneHanded it becomes
Light.

`CHOOSE:FEAT=Weapon Focus|1 <tab> BONUS:WEAPONPROF=%LIST|TOHIT|1`

Chooser for weapon's proficiency to add 1 to the to-hit of a Weapon
Focus.

`CHOOSE:FEAT=Greater Weapon Focus|1 <tab> BONUS:WEAPONPROF=%LIST|DAMAGE|2`

Chooser for weapon's proficiency to add 2 to the damager of a Weapon
Focus.

`BONUS:WEAPONPROF=Cannon|TOHIT|-2|TYPE=GunneryPenalty`

Subtracts two from the to hit of Cannons due to gunnery.

`BONUS:WEAPONPROF=Dagger|DAMAGEMULT:0|.5`

Increases the damage multiplier of the dagger weapon by half your
strength bonus when wielding it off handed.

`BONUS:WEAPONPROF=Unarmed Strike|WEAPONBAB|MonkLVL-BAB`

When applied to a monk, this will change the monk's BAB for Unarmed
Strike to the full BAB as if the monk were a fighter

