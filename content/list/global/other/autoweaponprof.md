+++
date = "2016-08-01"
title = "AUTOWEAPONPROF (Global: OTHER)"
original_url = "list/global/other.html#autoweaponprof"
categories = [ "all-tag", "other-tag" ]
+++

## Status

Updated 5.17.11

## Syntax

`AUTO:WEAPONPROF|x|x`

## Parameters

-   x: Text (Weapon name)
-   x: TYPE=Text (Weapon Type)
-   x: TYPE.Text (Weapon Type)
-   x: DEITYWEAPONS (Deity's favored weapon)



What it does
------------

-   This is a pipe-delimited (|) list of weapons, by name or weapon
    type, that are granted as free weapon proficiencies.
-   You can specify individual weapons or all weapons of a weapon
    proficiency type.
-   When including the `TYPE=Text` or `TYPE,Text` sub-tag you may use a
    period-delimted (.) list of weapon types. This will grant the
    character proficiency with weapons that meet all of the listed
    weapon types.
-   When using the `DEITYWEAPONS` sub-tag, all of the deity's favored
    weapons, except for natural weapons, are added. If the deity
    specifies "ALL" or "ANY" for its favored weapon, no weapons will
    be added.
-   PRExxx tags are allowed with this tag and use the pipe-delimited (|)
    syntax.

Examples
--------

`AUTO:WEAPONPROF|Longsword|Shortbow (Composite)`

The "Longsword" and "Shortbow (Composite)" are given as free weapon
proficiencies.

`AUTO:WEAPONPROF|TYPE.Simple`

All "Simple" weapons are given as free weapon proficiencies.

`AUTO:WEAPONPROF|TYPE.Simple|TYPE.Martial`

All "Simple" and "Martial" weapons are given as free weapon
proficiencies.

`AUTO:WEAPONPROF|TYPE.Ranged|TYPE.Piercing|TYPE.Simple`

All "Ranged", "Piercing" and "Simple" weapons are given as free weapon
proficiencies.

`AUTO:WEAPONPROF|TYPE.Martial.Slashing`

All "Martial" weapons that are "Slashing" type are given as free weapon
proficiencies.

`AUTO:WEAPONPROF|TYPE.Martial.Slashing.Melee`

All "Melee" type "Martial" weapons that are "Slashing" type are given as
free weapon proficiencies.

`AUTO:WEAPONPROF|DEITYWEAPONS`

All favored weapons of the character's deity are given as free weapon
proficiencies.

`AUTO:WEAPONPROF|TYPE=NoProfReq|Longspear|Javelin`

All "NoProfReq" and "Longspear" and "Javelin" weapons are given as free
weapon proficiencies.

`CLASS:Rogue.MOD <tab> AUTO:WEAPONPROF|Gladius`

Modified the Rogue Class to include the Gladius weapon.

