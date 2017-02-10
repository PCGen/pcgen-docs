+++
date = "2016-08-01"
title = "ALIGNMENT (Global: CHOOSE)"
original_url = "/list/global/choose.html#alignment"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "ALIGNMENT"
    parent = "global_choose"
+++

## Status

New 5.17.4

## Syntax

`CHOOSE:ALIGNMENT|x|x`

## Parameters

-   x: Text (Alignment by key)
-   x: FEAT=Text (Feat, by name or key)
-   x: TYPE=Text (Alignment type)
-   x: !TYPE=Text (Prohibited alignment type)
-   x: ALL



What it does
------------

-   This will produce a list of "Alignments" (e.g. LG, TN, CE, etc. for
    3.5e gameMode).
-   Use of the `FEAT` subtag will provide the alignment selected by the
    referenced feat. The feat referenced must contain a
    `CHOOSE:ALIGNMENT` tag.
-   Criteria can be logically combined by using the comma (,), logical
    **AND** , and the pipe (|), logical **OR** . Logical **AND** s are
    evaluated before logical **OR** s.
-   The [SELECT](/list/global/other/select.html) tag is used in
    conjunction with this `CHOOSE` tag to define the number of
    "selections" that can be made.

Example
-------

CHOOSE:ALIGNMENT|ALL

This will produce a list of all alignments available.

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

