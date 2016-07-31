+++
date = "2016-08-01"
title = "COMBAT (Global: BONUS)"
original_url = "list/global/bonus.html#combat"
categories = [ "all-tag", "bonus-tag" ]
+++

## Status

Updated 6.03.04

## Syntax

`BONUS:COMBAT|x|y`

## Parameters

-   x: AC
-   x: ATTACKS
-   x: BAB <span class="lstdep"> This sub-token is
    deprecated - Use BASEAB instead. </span>
-   x: BASEAB
-   x: DAMAGE.Text (Weapon or damage type)
-   x: DAMAGEMULT:Number (0 for off-hand, 1 for
    primary, and 2 for two-handed)
-   x: DAMAGESIZE
-   x: DAMAGE-SHORTRANGE
-   x: EPICAB
-   x: INITIATIVE
-   x: REACH
-   x: RANGEPENALTY
-   x: SECONDARYATTACKS
-   x: SECONDARYDAMAGE
-   x: TOHIT
-   x: TOHIT.Text (Weapon type)
-   x: TOHIT-PRIMARY
-   x: TOHIT-SECONDARY
-   x: TOHIT-SHORTRANGE
-   y: Number, Variable or Formula (Bonus value)



What it Does
------------

-   Adds to indicated combat bonus, i.e.:
    -   Using the `AC` syntax adds to the armor class.
    -   Using the `ATTACKS` syntax adds to the number of attacks the
        primary hand gets.
    -   Using the `BASEAB` syntax increases the base attack bonus and
        may increase the number of attacks the primary hand gets.
    -   Using the `DAMAGE` syntax increases the damage bonus but the
        weapon and damage types specified must be valid equipment types
        assigned to a weapon in the current data set or must have been
        defined by the `WEAPONTYPE` tag in the current gamemode.
        Examples of standard Weapon and Weapon Damage types can be found
        on the [Global Type](/list/global/type.html#equipment) page.
    -   Using the `DAMAGEMULT` syntax increases the damage multiplier
        for the designated hand(s) wielding the weapon. Bonuses are
        additive between each `BONUS` . Two
        `BONUS:COMBAT|DAMAGEMULT:0|1.5` tags will do a total of x3
        damage, not 2.25.
    -   Using the `DAMAGESIZE` syntax increases, or decreases, the
        damage die size along the same scale as is used for weapon size,
        i.e.:
        -   Base Damage Dice:1d2
            -   Scaling Up:1d3,1d4,1d6,1d8,2d6,3d6,4d6,6d6,8d6,12d6
            -   Scaling Down:1,0
        -   Base Damage Dice:1d3
            -   Scaling Up:1d4,1d6,1d8,2d6,3d6,4d6,6d6,8d6,12d6
            -   Scaling Down:1d2,1,0
        -   Base Damage Dice:1d4
            -   Scaling Up:1d6,1d8,2d6,3d6,4d6,6d6,8d6,12d6
            -   Scaling Down:1d3,1d2,1,0
        -   Base Damage Dice:1d6
            -   Scaling Up:1d8,2d6,3d6,4d6,6d6,8d6,12d6
            -   Scaling Down:1d4,1d3,1d2,1
        -   Base Damage Dice:1d8
            -   Scaling Up:2d6,3d6,4d6,6d6,8d6,12d6
            -   Scaling Down:1d6,1d4,1d3,1d2
        -   Base Damage Dice:1d10
            -   Scaling Up:2d8,3d8,4d8,6d8,8d8,12d8
            -   Scaling Down:1d8,1d6,1d4,1d3
        -   Base Damage Dice:1d12
            -   Scaling Up:3d6,4d6,6d6,8d6,12d6
            -   Scaling Down:1d10,1d8,1d6,1d4
        -   Base Damage Dice:2d4
            -   Scaling Up:2d6,3d6,4d6,6d6,8d6,12d6
            -   Scaling Down:1d6,1d4,1d3,1d2
        -   Base Damage Dice:2d6
            -   Scaling Up:3d6,4d6,6d6,8d6,12d6
            -   Scaling Down:1d10,1d8,1d6,1d4
        -   Base Damage Dice:2d8
            -   Scaling Up:3d8,4d8,6d8,8d8,12d8
            -   Scaling Down:2d6,1d10,1d8,1d6
        -   Base Damage Dice:2d10
            -   Scaling Up:4d8,6d8,8d8,12d8
            -   Scaling Down:2d8,2d6,1d10,1d8
    -   Using the `DAMAGE-SHORTRANGE` syntax adds to the damage of a
        weapon at short range as defined in the GameMode files.
    -   Using the `EPICAB` syntax increases the epic attack bonus and
        may increase the number of attacks the primary hand gets.
    -   Using the `INITIATIVE` syntax increases the
        character's initiative.
    -   Using the `REACH` syntax modifies the character's reach.
    -   Using the `RANGEPENALTY` syntax modifies the character's range
        increment penalty.
    -   Using the `SECONDARYATTACKS` syntax increases the number of
        secondary attacks.
    -   Using the `SECONDARYDAMAGE` syntax increases the damage modifier
        for secondary attacks.
    -   Using the `TOHIT` syntax increases the primary attack bonus.
    -   Using the `TOHIT.x` syntax increases the attack bonus for the
        designated attack, i.e. by weapon type, grapple, melee, or
        ranged attack.
    -   Using the `TOHIT-PRIMARY` syntax increases the primary
        attack bonus.
    -   Using the `TOHIT-SECONDARY` syntax increases the secondary
        attack bonus.
    -   Using the `TOHIT-SHORTRANGE` syntax adds to the ranged attack
        rolls that are less than the gamemode defined **SHORTRANGE** but
        does not affect attacks per round.

Examples
--------

`BONUS:COMBAT|AC|2|TYPE=Enhancement`

Increases the enhancement armor bonus by two.

`BONUS:COMBAT|AC|7|TYPE=NaturalArmor.REPLACE`

Replaces the natural armor bonus to seven.

`BONUS:COMBAT|ATTACKS|2`

Increases number of attacks by two.

`BONUS:COMBAT|BASEAB|1`

Increases base attack bonus by one.

`BONUS:COMBAT|BAB|CL|TYPE=Base.REPLACE`

Increases base attack bonus by Character Level, replacing the Base
value.

`BONUS:COMBAT|DAMAGE.Piercing|2`

Increases "Piercing" damage bonus by two.

`BONUS:COMBAT|DAMAGE.Unarmed,DAMAGE.Thrown|DEX`

Adds the character's dexterity modifier to both "Unarmed" and "Thrown"
damage.

`BONUS:COMBAT|DAMAGEMULT:0|0.5`

Increases the damage multiplier by half your strength bonus. Combined
with the existing bonus this bonus will total your full strength bonus
for an off hand weapon.

`BONUS:COMBAT|DAMAGEMULT:1|1`

Increases the damage multiplier of the weapon by your strength bonus
when wielding in your primary hand.

`BONUS:COMBAT|DAMAGEMULT:2|1.5`

Increases the damage multiplier of the weapon by one and a half your
strength bonus when wielding it two-handed.

`BONUS:COMBAT|DAMAGESIZE|2`

If the base damage dice is 1d8 this would scale it up to 3d6.

`BONUS:COMBAT|DAMAGESIZE|-1`

If the base damage dice is 1d4 this would scale it down to 1d3.

`BONUS:COMBAT|DAMAGE-SHORTRANGE|1`

Increases the damage done by a weapon at short range by 1.

`BONUS:COMBAT|EPICAB|1`

Increases epic attack bonus by one.

`BONUS:COMBAT|INITIATIVE|3`

Increases initiative by three.

`BONUS:COMBAT|INITIATIVE|2|TYPE=Competence`

Increases initiative by two for Competence.

`BONUS:COMBAT|REACH|10`

Increases reach by ten feet.

`BONUS:COMBAT|RANGEPENALTY|1`

Reduces the range increment penalty by 1 (for example from -2 to -1).

`BONUS:COMBAT|RANGEPENALTY|-2`

Increases the range increment penalty by 2 (for example from -2 to -4).

`BONUS:COMBAT|SECONDARYATTACKS|1`

Increases secondary attacks by one.

`BONUS:COMBAT|SECONDARYDAMAGE|2`

Increases the secondary attack damage bonus by two.

`BONUS:COMBAT|TOHIT|2|TYPE=Luck`

Increases Attack bonus by two.

`CHOOSE:WEAPONPROFS|3 <tab> BONUS:COMBAT|TOHIT.%LIST|1|TYPE=Talent`

Increases Attack bonus by one for three WEAPONPROFS based on Talent.

`BONUS:COMBAT|TOHIT.THROWN|2|TYPE=Racial`

Increases Attack for thrown weapon's bonus by two.

`BONUS:COMBAT|TOHIT.SLASHING|2|TYPE=Enhancement`

Increases Attack bonus by two when using a Slashing weapon.

`BONUS:COMBAT|TOHIT-PRIMARY|2`

Increases Primary Attack bonus by two.

`BONUS:COMBAT|TOHIT-SECONDARY|1`

Increases Secondary Attack bonus by one.

`BONUS:COMBAT|TOHIT-SHORTRANGE|1`

Adds one to character's short range To-Hit attack rolls.

**Deprecated Syntax:** <span class="lstdep"> Remove for 6.6 </span>

`BONUS:COMBAT|BAB|1`

Becomes `BONUS:COMBAT|BASEAB|1`

