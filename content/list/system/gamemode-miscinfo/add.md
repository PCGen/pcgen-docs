+++
date = "2016-08-01"
title = "ADD (Game Mode: miscinfo.lst)"
original_url = "/list/system/gamemode-miscinfo.html#add"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
[menu.main]
    name = "ADD"
    parent = "system_gamemode-miscinfo"
+++

## Status

New 5.4

## Syntax

`ADD:x`

## Parameters

-   x: Text (Name of a defined Armor Class Type).



**Pre defined ACTYPEs:**

-   Ability
-   Armor
-   Base
-   ClassDefense
-   Dodge
-   NaturalArmor
-   Shield
-   Total

What it does
------------

The ADD tag is used in lines beginning with ACTYPE. The ADD tag adds the
defined ACTYPE specified to the ACTYPE being defined by the ACTYPE line.
The ADD tag can be qualified with PRExxx tags.

Example
-------

`ADD:TOTAL`

Adds ACTYPE:TOTAL to the ACTYPE being defined in the ACTYPE line.

`ADD:Shield`

Adds ACTYPE:SHIELD to the ACTYPE being defined in the ACTYPE line.

