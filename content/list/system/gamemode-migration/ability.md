+++
date = "2016-08-01"
title = "ABILITY (Game Mode: migration.lst)"
original_url = "/list/system/gamemode-migration.html#ability"
categories = [ "all-tag", "gamemode-migration-tag" ]
[menu.main]
    name = "ABILITY (Game Mode: migration.lst)"
    parent = "gamemode-migration"
+++

## Status

New 6.01.03

## Syntax

`ABILITY:x|y`

## Parameters

-   x: Text (Old Ability Category)
-   y: Text (Old Ability Key)



What it does
------------

-   This tag begins an ability migration line and is used to identify
    the old ability key as part of the migration to a new ability key.
-   The `ABILITY` tag is used in conjunction with the
    [NEWKEY](/list/system/gamemode-migration/newkey.html) ,
    [NEWCATEGORY](/list/system/gamemode-migration/newcategory.html) ,
    and version tags.

Example
-------

`ABILITY:Special Ability|Animal Fury`



