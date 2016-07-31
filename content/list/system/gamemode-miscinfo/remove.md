+++
date = "2016-08-01"
title = "REMOVE (Game Mode: miscinfo.lst)"
original_url = "list/system/gamemode-miscinfo.html#remove"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
+++

## Status

New 5.4

## Syntax

`REMOVE:x`

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

The REMOVE tag is used in lines beginning with ACTYPE. The REMOVE tag
subtracts the defined ACTYPE specified to the ACTYPE being defined by
the ACTYPE line. The REMOVE tag can be qualified with PRExxx tags.

Example
-------

`REMOVE:Base`

Subtracts ACTYPE:Base to the ACTYPE being defined in the ACTYPE line.

`REMOVE:Shield`

Subtracts ACTYPE:Shield to the ACTYPE being defined in the ACTYPE line.

