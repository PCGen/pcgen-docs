+++
date = "2016-08-01"
title = "DOMAIN (Global: CHOOSE)"
original_url = "/list/global/choose.html#domain"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "DOMAIN (Global: CHOOSE)"
    parent = "choose"
+++

## Status

Updated 5.17.4

## Syntax

`CHOOSE:DOMAIN|x|y|y[x]|y[x,x]|x,y,y[x],y[x,x]`

## Parameters

-   x: Text (Domain name or key)
-   x: DEITY=Text (Deity name)
-   x: FEAT=Text (Feat, by name or key)
-   x: TYPE=Text (Domain type)
-   x: !TYPE=Text (Prohibited domain type)
-   x: ALL
-   y: ANY (Default)
-   y: PC
-   y: QUALIFIED



What it does
------------

-   Will present a list of domains that match the stipulated criteria.
-   Using the `DEITY=Text` sub-tag will provide a list of domains for
    the referenced deity.
-   Using the `FEAT=Text` sub-tag will provide a list of domains
    selected by the referenced feat. The feat referenced must contain a
    `CHOOSE:DOMAIN` tag.
-   Global qualifiers work for equipment. Use of the qualifiers has the
    following effect:
    -   **ANY** - Will return a list of all domains.
    -   **PC** - Will return the name of the domains already taken by
        the Player Character.
    -   **QUALIFIED** - Will return a list of all domains that the
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

`CHOOSE:DOMAIN|Air|Fire|Sun`

A list of domains including **Air** , **Fire** and **Sun** domains will
be presented.

`CHOOSE:DOMAIN|DIETY=Kong`

A list of domains granted by the deity **Kong** will be presented.

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

