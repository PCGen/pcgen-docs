+++
date = "2016-08-01"
title = "CATEGORY (Game Mode: miscinfo.lst)"
original_url = "list/system/gamemode-miscinfo.html#category"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
+++

## Status

New 5.11.1

## Syntax

`CATEGORY:x`

## Parameters

-   x: Text (Ability category name.).



What it does
------------

-   Used to define the "parent" ability category that the new category
    is a sub-category of.
-   The parent category must exist and be loaded into PCGen.
-   For abilities that use `MULT:YES` , the parent category must be
    defined without a TYPE in order to funtion properly, with respect to
    the `MULT:YES` tag.
-   This tag is optional.

Example
-------

`CATEGORY:Feat`

The parent ability category for this category is Feat.

Where it is used
----------------

Used in
[ABILITYCATEGORY](/list/system/gamemode-miscinfo/abilitycategory.html)
lines.

