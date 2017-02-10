+++
date = "2016-08-01"
title = "CLASS (Global: CHOOSE)"
original_url = "/list/global/choose.html#class"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "CLASS"
    parent = "global_choose"
+++

## Status

Updated 5.17.4

## Syntax

`CHOOSE:CLASS|x|y|y[x]|y[x,x]|x,y,y[x],y[x,x]`

## Parameters

-   x: Text (Class name or key)
-   x: FEAT=Text (Feat, by name or key)
-   x: SPELLTYPE=Text (Spell type)
-   x: SPELLCASTER
-   x: TYPE=Text (Class type)
-   x: !TYPE=Text (Prohibited ability type)
-   x: ALL
-   y: ANY (Default)
-   y: PC
-   y: QUALIFIED



What it does
------------

-   Will present a list of classes that matche the stipulated criteria.
-   Using the `FEAT=Text` sub-tag will provide a list of classes chosen
    by the referenced feat. The feat referenced must contain a
    `CHOOSE:CLASS` tag.
-   Using the `SPELLTYPE=Text` sub-tag will provide a list of classes
    that cast spells of the designated type.
-   Using the `SPELLCASTER` sub-tag will provide a list of classes that
    can cast spells.
-   Global qualifiers work with abilities. Use of the qualifiers has the
    following effect:
    -   **ANY** - Will return a list of all classes.
    -   **PC** - Will return a list of all classes already selected by
        the Player Character.
    -   **QUALIFIED** - Will return a list of all classes that the
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

`CHOOSE:CLASS|TYPE=Prestige,PC`

A list of all **Prestige** type classes that the PC has will be
presented.

`CHOOSE:CLASS|Wizard|Fighter`

A list of all classes consisting of the **Wizard** and **Fighter**
classes will be presented.

`CHOOSE:CLASS|Fighter|TYPE=Prestige,PC`

A list of all **Prestige** type classes that the PC has plus the
**Fighter** class will be presented.

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

