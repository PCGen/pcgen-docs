+++
date = "2016-08-01"
title = "WEAPONPROFICIENCY (Global: CHOOSE)"
original_url = "/list/global/choose.html#weaponproficiency"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "WEAPONPROFICIENCY"
    parent = "global_choose"
+++

## Status

New 5.17.4

## Syntax

`CHOOSE:WEAPONPROFICIENCY|x|y|y[x]|y[x,x]|x,y,y[x],y[x,x]`

## Parameters

-   x: Text (Weapon proficiency)
-   x: DEITYWEAPON (Feat, by name or key)
-   x: FEAT=Text (Feat, by name or key)
-   x: WIELD=Text (Weapon wield type. Used in
    `EQUIPMENT` qualifier only.)
-   x: TYPE=Text (Weapon proficiency type)
-   x: !TYPE=Text (Prohibited weapon proficiency type)
-   x: ALL
-   y: ANY (Default)
-   y: PC
-   y: QUALIFIED
-   y: EQUIPMENT\[x\] (Special qualifier)
-   y: SPELLCASTER\[x\] (Special qualifier)



What it does
------------

-   This will produce a list of all weapon proficiencies matching
    the criteria.
-   Using the `DEITYWEAPON` sub-tag will provide the weapon listed as
    the favored weapon for the player character's selected deity.
-   Using the `FEAT=Text` sub-tag will provide a list of weapon
    proficiencies selected by the referenced feat. The feat referenced
    must contain a `CHOOSE:WEAPONPROFICIENCY` tag.
-   Using the `WIELD=Text` sub-tag will provide a list of weapon
    proficiencies for weapons of the referenced wield type. The wield
    type must one of the following three types: Light,
    One-Handed, Two-Handed. **WIELD** type is set for each weapon in the
    equipment LST file.
-   Using the `WIELD=Text` sub-tag in an `EQUIPMENT` qualifier will
    provide a list of weapon proficiencies for weapons of the referenced
    wield type. The wield type must one of the following three types:
    Light, One-Handed, Two-Handed. Wield type is set for each weapon in
    the equipment LST file. Note: Not all game modes support `WIELD` .
-   Using the `EQUIPMENT` qualifier will allow the selection of
    proficiencies based on weapons. It can be combined with `TYPE=Text`
    and `WIELD=Text` criteria, contained in square-brackets (\[x\]) to
    restrict the proficiencies offered.
-   When using the `SPELLCASTER` qualifier will provide a list of
    proficiencies matching the included criteria as long as the player
    character is a spellcaster.
-   Global qualifiers work for weapon proficiencies. Use of the
    qualifiers has the following effect:
    -   **ANY** - Will return a list of all weapon proficiencies.
    -   **PC** - Will return a list of all weapon proficiencies already
        taken by the Player Character.
    -   **QUALIFIED** - Will return a list of all weapon proficiencies
        that the player character is otherwise qualified for.
-   Qualifiers can be logically negated by prefacing with the
    exclamation point (!), i.e. `!PC` is a valid usage.
-   Criteria can be logically combined by using the comma (,), logical
    **AND** , and the pipe (|), logical **OR** . Logical **AND** s are
    evaluated before logical **OR** s.
-   The [SELECT](/list/global/other/select.html) tag is used in
    conjunction with this `CHOOSE` tag to define the number of
    "selections" that can be made.

Example
-------

`CHOOSE:WEAPONPROFICIENCY|Longsword|Flail`

Will display a list of weapon proficiencies including only **Longsword**
and **Flail** .

`CHOOSE:WEAPONPROFICIENCY|Longsword|TYPE=Ranged,PC`

Will display a list of weapon proficiencies of the **Ranged** type that
the PC is already proficient with.

`CHOOSE:WEAPONPROFICIENCY|SPELLCASTER[Ray]`

Will add proficiency with the **Ray** if the PC is a spellcaster.

`CHOOSE:WEAPONPROFICIENCY|EQUIPMENT[TYPE=Finesseable]`

Will display a list of weapon proficiencies for all weapons with a type
of **Finesseable** .

`CHOOSE:WEAPONPROFICIENCY|EQUIPMENT[TYPE=Melee,WIELD=Light]`

Will display a list of weapon proficiencies for all weapons with a type
of Melee that also have a wield type of **Light** .

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

