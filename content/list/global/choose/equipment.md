+++
date = "2016-08-01"
title = "EQUIPMENT (Global: CHOOSE)"
original_url = "list/global/choose.html#equipment"
categories = [ "all-tag", "choose-tag" ]
+++

## Status

New 6.03.02

## Syntax

`CHOOSE:EQUIPMENT|x|y|y[x]|y[x,x]|x,y,y[x],y[x,x]`

## Parameters

-   x: Text (Equipment name or key)
-   x: WIELD=Text (Equipment wield type)
-   x: TYPE=Text (Equipment type)
-   x: !TYPE=Text (Equipment type)
-   x: ALL
-   y: ANY (Default)
-   y: OWNED
-   y: QUALIFIED
-   y: CARRIED
-   y: EQUIPPED



What it does
------------

-   Will present a list of equipment that matches the
    stipulated criteria.
-   Using the `WIELD=Text` sub-tag will provide a list of equipment of
    the referenced wield type. The wield type must one of the following
    three types: Light, One-Handed, Two-Handed.
-   Global qualifiers work for equipment. Use of the qualifiers has the
    following effect:
    -   **ANY** - Will return a list of all equipment.
    -   **OWNED** - Will return a list of all equipment already taken by
        the Player Character whether carried or equipped.
    -   **QUALIFIED** - Will return a list of all equipment that the
        player character is otherwise qualified for.
    -   **CARRIED** - Will return a list of all equipment that the
        player character has, is carrying, but is not equipped.
    -   **EQUIPPED** - Will return a list of all equipment that the
        player character has and is equipped.
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

`CHOOSE:EQUIPMENT|TYPE=Melee.Simple`

A list of all "Simple" and "Melee" type feats will be presented.

`CHOOSE:EQUIPMENT|TYPE=Simple,OWNED`

A list of all simple equipment that the PC has already selected will be
presented.

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files. For the eqmod version
see [CHOOSE:EQUIPMENT (Equipment
Modifiers)](/list/data/equipmentmodifiers/chooseequipment.html)

