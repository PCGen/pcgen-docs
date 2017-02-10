+++
date = "2016-08-01"
title = "SIZE (Global: CHOOSE)"
original_url = "/list/global/choose.html#size"
categories = [ "all-tag", "choose-tag" ]
[menu.main]
    name = "SIZE"
    parent = "global_choose"
+++

## Status

New 5.17.4

## Syntax

`CHOOSE:SIZE|x|x`

## Parameters

-   x: Text (Size)
-   x: TYPE=Text (Size type)
-   x: !TYPE=Text (Prohibited size type)
-   x: ALL



What it does
------------

-   This will produce a list of sizes (e.g. Small, Colossal, etc).
-   The size list is a pipe (|) delimited list representing the logical
    **OR** .

Example
-------

`CHOOSE:SIZE|ALL`

This will produce a list of all sizes available in the gameMode.

Where it is Used
----------------

Ability, Domain, Feat, Race, and Template files.

