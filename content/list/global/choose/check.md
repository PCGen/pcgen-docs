+++
date = "2016-08-01"
title = "CHECK (Global: CHOOSE)"
original_url = "/list/global/choose.html#check"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "CHECK"
    parent = "global_choose"
    identifier = "global_choose_CHECK"
+++

## Status

New 5.17.4

## Syntax

`CHOOSE:CHECK|x|x`

## Parameters

-   x: Text (Check by KEY)
-   x: FEAT=Text (Feat, by name or key)
-   x: TYPE=Text (Check type)
-   x: !TYPE=Text (Prohibited check type)
-   x: ALL



What it does
------------

-   This will produce a list of checks (e.g. Will, Reflex, etc).
-   Use of the `FEAT` subtag will provide the stat selected by the
    referenced feat. The feat referenced must contain a
    `CHOOSE:CHECK` tag.
-   Criteria can be logically combined by using the comma (,), logical
    **AND** , and the pipe (|), logical **OR** . Logical **AND** s are
    evaluated before logical **OR** s.
-   The [SELECT](/list/global/other/select.html) tag is used in
    conjunction with this `CHOOSE` tag to define the number of
    "selections" that can be made.

Example
-------

`CHOOSE:CHECK|ALL`

This will produce a list of all checks available in the gameMode.

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

