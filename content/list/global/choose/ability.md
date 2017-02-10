+++
date = "2016-08-01"
title = "ABILITY (Global: CHOOSE)"
original_url = "/list/global/choose.html#ability"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "ABILITY"
    parent = "global_choose"
+++

## Status

Updated 5.17.4

## Syntax

`
CHOOSE:ABILITY|w|x|y|y[x]|y[x,x]|x,y,y[x],y[x,x]`

## Parameters

-   w: Text (Ability category)
-   x: Text (Ability name or key)
-   x: FEAT=Text (Feat, by name or key)
-   x: TYPE=Text (Ability type)
-   x: !TYPE=Text (Prohibited ability type)
-   x: ALL
-   y: ANY (Default)
-   y: PC
-   y: QUALIFIED



What it does
------------

-   Will present a list of abilities of the specified category that
    matches the stipulated criteria.
-   Using the `FEAT=Text` sub-tag will provide a list of abilities
    chosen by the referenced feat. The feat referenced must contain a
    `CHOOSE:ABILITY` tag.
-   Global qualifiers work with abilities. Use of the qualifiers has the
    following effect:
    -   **ANY** - Will return a list of all abilities of the designated
        ability category.
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

`CHOOSE:ABILITY|FEAT|TYPE=Rogue Abilities`

A list of all "Rogue Abilities" type feats will be presented.

`CHOOSE:ABILITY|Special Ability|PC[TYPE=Mercy]`

A list of all "Mercy" type abilities will be presented.

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files. For the eqmod version
see [CHOOSE:EQUIPMENT (Equipment
Modifiers)](/list/data/equipmentmodifiers/chooseequipment.html)

