+++
date = "2016-08-01"
title = "DISPLAYLOCATION (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#displaylocation"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "DISPLAYLOCATION"
    parent = "system_gamemode-miscinfo"
+++

## Status

New 5.13.2

## Syntax

`DISPLAYLOCATION:x`

## Parameters

-   x: Text (The sub tab name or key to the sub
    tab name)



What it does
------------

-   Used to define the name of the sub-tab that the ability category
    will be displayed on. The tag allows related categories to be
    grouped onto the same subtab.
-   This tag is optional, and if not present the ability category's
    plural name will be used instead.
-   Support for internationalization can be achieved by using a sub-tab
    key in the form of "in\_&lt;name&gt;", i.e. "in\_feats".

Example
-------

`DISPLAYLOCATION:in_feat`

Abilities of the associated category will be displayed in the feats
sub-tab, which is identified by the sub-tab key "in\_feat".

Where it is used
----------------

Used in
[ABILITYCATEGORY](/list/system/gamemode-miscinfo/abilitycategory.html)
lines.

