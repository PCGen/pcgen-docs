+++
date = "2016-08-01"
title = "CLASS (System: bio/biosettings.lst)"
original_url = "/list/system/biosettings.html#class"
categories = [ "all-tag", "biosettings-tag" ]
[menu.main]
    name = "CLASS"
    parent = "system_biosettings"
+++

## Status

None

## Syntax

`CLASS:x,x[BASEAGEADD:y]`

## Parameters

-   x: Text (Class name)
-   y: Number (The die-roll to be added to the BASEAGE
    based upon the class)



What it does
------------

Used in AGESET:0 to define the number of years to add to the base age,
for each character class of this race.

Example
-------

`CLASS:Barbarian,Rogue,Sorcerer[BASEAGEADD:1d4]`

If the class is "Barbarian", "Rogue" or "Sorcerer" than the add 1d4 to
the base age.

