+++
date = "2016-08-01"
title = "DEITY (Global: CHOOSE)"
original_url = "/list/global/choose.html#deity"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "DEITY"
    parent = "global_choose"
    identifier = "global_choose_DEITY"
+++

## Status

New 5.17.4

## Syntax

`CHOOSE:DEITY|x|y|y[x]|y[x,x]|x,y,y[x],y[x,x]`

## Parameters

-   x: Text (Deity name or key)
-   x: ALIGN=Text (Alignment abbreviation)
-   x: FEAT=Text (Feat, by name or key)
-   x: PANTHEON=Text (Pantheon name)
-   x: TYPE=Text (Deity type)
-   x: !TYPE=Text (Prohibited deity type)
-   x: ALL
-   y: ANY (Default)
-   y: PC
-   y: QUALIFIED



What it does
------------

-   Will present a list of deities that matches the stipulated criteria.
-   Using the `ALIGN=Text` sub-tag will provide a list of deities of the
    referenced alignment.
-   Using the `FEAT=Text` sub-tag will provide a list of deities
    selected by the referenced feat. The feat referenced must contain a
    `CHOOSE:DEITY` tag.
-   Using the `PANTEON=Text` sub-tag will provide a list of deities of
    the referenced pantheon.
-   Global qualifiers work for equipment. Use of the qualifiers has the
    following effect:
    -   **ANY** - Will return a list of all deities.
    -   **PC** - Will return the name of the deity already taken by the
        Player Character.
    -   **QUALIFIED** - Will return a list of all deities that the
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

`CHOOSE:DEITY|Set|Ra`

A list of the deities **Set** and **Ra** will be presented.

`CHOOSE:DEITY|Set,Ra`

No deity list will be presented because no deity can be both **Set** and
**Ra** .

`CHOOSE:DEITY|PANTHEON=Olympian,ALIGN=LG`

A list of all **Lawful Good** deities of the **Olympian** pantheon will
be presented.

`CHOOSE:DEITY|TYPE=Good,PC`

A list of all **Good** type deities that the PC has already selected
will be presented.

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

