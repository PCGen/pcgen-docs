+++
date = "2016-08-01"
title = "ACTYPE (Game Mode: miscinfo.lst)"
original_url = "list/system/gamemode-miscinfo.html#actype"
categories = [ "all-tag", "gamemode-miscinfo-tag" ]
+++

## Status

New 5.4

## Syntax

`ACTYPE:x`

## Parameters

-   x: Text (Name of the Armor Class Type being defined
    by the line).



What it does
------------

ACTYPE begins a new line will which defines which AC will be made
available to output sheets, and how to calculate this AC.

A line beginning with ACTYPE will include an
[ADD](/list/system/gamemode-miscinfo/add.html) tag and may also include
a [REMOVE](/list/system/gamemode-miscinfo/remove.html) tag.

**Syntax:**

`ACTYPE:Name ADD:List Remove:List`

Example
-------

`ACTYPE:Total ADD:TOTAL`

Defines the ACTYPE Total as the Total AC bonuses

`ACTYPE:Touch ADD:TOTAL REMOVE:Armor|NaturalArmor|Shield`

Defines the ACTYPE Touch as the Total AC minus Armor, NaturalArmor and
Shield bonuses

