+++
date = "2016-08-01"
title = "FEATSELECTION (Global: CHOOSE)"
original_url = "/list/global/choose.html#featselection"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "FEATSELECTION (Global: CHOOSE)"
    parent = "choose"
+++

## Status

New 5.17.3

## Syntax

`CHOOSE:FEATSELECTION|w|x|y|y[z]|y[x,x]|x,y,y[x],y[x,x]`

## Parameters

-   w: TITLE=Text (Chooser title)
-   x: Text (Feat name or key)
-   x: TYPE=Text (Feat type)
-   x: !TYPE=Text (Prohibited Feat type)
-   x: ALL
-   y: ANY (Default)
-   y: PC
-   y: QUALIFIED



What it does
------------

-   This will produce a list of feats, resolved down to the internal
    feat selections, matching the stipulated criteria.
-   Global qualifiers work for feats. Use of the qualifiers have the
    following effect:
    -   **ANY** - Will return a list of all feats.
    -   **PC** - Will return a list of all feats already taken by the
        Player Character.
    -   **QUALIFIED** - Will return a list of all feats that the player
        character is otherwise qualified for.
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

`CHOOSE:FEATSELECTION|Dodge|Toughness`

Will display a list of feats comprised of the "Dodge" and "Toughness"
feats.

`CHOOSE:FEATSELECTION|TYPE=Fighter,PC`

This will produce a list of all the character's fighter feats.

`CHOOSE:FEATSELECTION|PC[TYPE=Fighter]`

This will produce a list of all the character's fighter feats.

`CHOOSE:FEATSELECTION|TYPE=Fighter`

This will produce a list of all fighter feats.

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

