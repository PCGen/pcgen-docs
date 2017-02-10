+++
date = "2016-08-01"
title = "ABILITYSELECTION (Global: CHOOSE)"
original_url = "/list/global/choose.html#abilityselection"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "ABILITYSELECTION"
    parent = "global_choose"
+++

## Status

New 6.01.03

## Syntax

`CHOOSE:ABILITYSELECTION|v|w|x|y|y[z]|y[x,x]|x,y,y[x],y[x,x]`

## Parameters

-   v: TITLE=Text (Chooser title)
-   w: Text (Ability Category)
-   x: Text (Ability Name or Key)
-   x: TYPE=Text (Ability type)
-   x: !TYPE=Text (Prohibited Ability type)
-   x: ALL
-   y: ANY (Default)
-   y: PC
-   y: QUALIFIED



What it does
------------

-   This will produce a list of abilities, resolved down to the internal
    ability selections, matching the stipulated criteria.
-   Global qualifiers work for abilities. Use of the qualifiers have the
    following effect:
    -   **ANY** - Will return a list of all abilities.
    -   **PC** - Will return a list of all abilities already taken by
        the Player Character.
    -   **QUALIFIED** - Will return a list of all abilities that the
        player character is otherwise qualified for.
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

`CHOOSE:ABILITYSELECTION|FEAT|Weapon Focus`

Will display a list of feats comprised of the "Dodge" and "Toughness"
feats.

`CHOOSE:ABILITYSELECTION|Ranger ~ Favored Enemy,PC`

This will produce a list of all the character's favored enemies.

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

