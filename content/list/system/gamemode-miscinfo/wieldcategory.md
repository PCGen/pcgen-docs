+++
date = "2016-08-01"
title = "WIELDCATEGORY (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#wieldcategory"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "WIELDCATEGORY"
    parent = "system_gamemode-miscinfo"
+++

## Status

New 5.5.2

## Syntax

`WIELDCATEGORY:x`

## Parameters

-   x: Text (Name of wield category)



What it does
------------

Defines how PCGen handles differences between PC size and Weapon size
based on the weapons WIELD tag.

Name is the target of the weapons WIELD tag such as 'Light', 'OneHanded'
or 'TwoHanded'.

There are three computation categories defined, 'Unusable', 'TooLarge'
and 'TooSmall' which are used for oversized or undersized weapons.

WIELDCATEGORY defines the name of the weapon category and is the first
tag in the line, the following tags can be used after WIELDCATEGORY to
define other attributes of the weapon category: HANDS, FINESSEABLE,
SIZEDIFF, DAMAGEMULT, PREVARxxx and SWITCH.

Example
-------

`WIELDCATEGORY:Light`

Defines 'Light' weapon category.

