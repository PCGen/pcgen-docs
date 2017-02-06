+++
date = "2016-08-01"
title = "NEWCATEGORY (Game Mode: migration.lst)"
original_url = "/list/system/gamemode-migration.html#newcategory"
categories = [ "all-tag", "gamemode-migration-tag" ]
[menu.main]
    name = "NEWCATEGORY (Game Mode: migration.lst)"
    parent = "gamemode-migration"
+++

## Status

New 6.01.03

## Syntax

`NEWCATEGORY:x`

## Parameters

-   x: Text (New Ability Category)



What it does
------------

-   This tag is used in an ability migration line to identify the new
    category for the associated ability object when the ability
    category changes.
-   If this tag is not included in the ability migration line the
    ability category will not change for the associated ability.

Example
-------

`NEWCATEGORY:Spell-like Ability`



