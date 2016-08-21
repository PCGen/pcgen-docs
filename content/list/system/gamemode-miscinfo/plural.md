+++
date = "2016-08-01"
title = "PLURAL (Game Mode: miscinfo.lst)"
original_url = "list/system/gamemode-miscinfo.html#plural"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
+++

## Status

New 5.11.1

## Syntax

`PLURAL:x`

## Parameters

-   x: Text (The plural name or key to the plural name)



What it does
------------

Used in
[ABILITYCATEGORY](/list/system/gamemode-miscinfo/abilitycategory.html)
lines to define the plural name for this category. If this tag is set to
in\_name (ie: in\_feats) it will pull the plural name from the language
files (for internationalization).

Example
-------

`PLURAL:in_feats`

The plural name for the category is the value in the selected language
for the key in\_feats.

Where it is used
----------------

Used in
[ABILITYCATEGORY](/list/system/gamemode-miscinfo/abilitycategory.html)
lines.

