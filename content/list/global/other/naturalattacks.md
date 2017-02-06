+++
date = "2016-08-01"
title = "NATURALATTACKS (Global: OTHER)"
original_url = "/list/global/other.html#naturalattacks"
categories = [ "all-tag", "other-tag" ]
[menu.main]
    name = "NATURALATTACKS (Global: OTHER)"
    parent = "other"
+++

## Status

Updated 6.1.9

## Syntax

`NATURALATTACKS:v,w.w,x,y,z|v,w.w,x,y,z`

## Parameters

-   v: Text (Natural weapon name)
-   w: Text (Natural weapon type)
-   x: Number (Number of attacks)
-   y: Text (Natural weapon damage)
-   z: SPROP=Text (special property
    description, Optional)



What it does
------------

-   This tag is used to define natural attacks and add them to the
    character when the containing object is assigned to the character.
-   This is a comma (,) and pipe-delimited (|) list of the natural
    attacks a creature has.
-   -   Pipes (|) are used to separate the entries of
        individual attacks.
    -   Commas are used to separate the parameters within a single
        attack listing. All four parameters, separated by three commas,
        must be present.
-   For multiple attacks included in the same `NATURALATTACKS` tag, the
    first is treated as a primary weapon and the second is treated as a
    secondary attack.
-   Natural weapon types (w) should be period-delimited (.). This must
    always start with "Weapon" and "Natural" and must be followed by
    either "Melee" or "Ranged". After that the weapon's damage types are
    listed which can be "Bludgeoning", "Piercing" or "Slashing" or any
    combination of the three.
-   If the number of attacks (x) has an asterisk in front of the number
    it indicates that the number of attacks is non-iterative, that is it
    is not based on the creature's attack progression but rather how
    many of the natural weapons it possesses.
-   The damage the natural weapon does is entered in the standard dice
    notation such as "1d8" and "4d10".
-   The SPROP= tag (z) allows special properties of the attack to
    be described. This might be "SPROP=plus poison" or "SPROP=plus 1d6
    fire" . Note there is no variable or prereq support, unlike
    equipment SPROP entries.
-   If this tag is applied through a race or template object, the "size"
    of the character is determined through those objects, otherwise, the
    attacks will always be size "Medium".
-   The `NATURALATTACKS` tag creates a proficiency for the attacks on
    the fly which allows the use of the `BONUS:WEAPONPROF` tag to
    effect it. For example, if you used the `NATURALATTACKS` tag to
    create a Bite attack you could then use
    `BONUS:WEAPONPROF=Bite|DAMAGE,TOHIT|2` to add 2 to the attack and
    damage rolls.

Example
-------

`NATURALATTACKS:Claw,Weapon.Natural.Melee.Piercing.Slashing,*2,1d4|Bite,Weapon.Natural.Melee.Bludgeoning.Piercing.Slashing,*1,1d6`

Race has 2 Claw attacks and a Bite attack.

`NATURALATTACKS:Slam,Weapon.Natural.Melee.Bludgeoning,*1,2d4,SPROP=plus 1d4 acid and grab`

Race has a single slam attack that has the extra information that it
does 1d4 acid and grab.

Where it is Used
----------------

Ability, Feat, Race, and Template files.

