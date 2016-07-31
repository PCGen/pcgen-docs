+++
date = "2016-08-01"
title = "PREARMORTYPE (Global: PRErequisite)"
original_url = "list/global/pre.html#prearmortype"
categories = [ "all-tag", "pre-tag" ]
+++

## Status

New 5.10

## Syntax

`PREARMORTYPE:x,y,y`

## Parameters

-   x: Number (The number of equipped armors needed).
-   y: Text (The name of an Armor).
-   y: Text (The name of a piece of Armor - "%" may be
    used as a wild-card).
-   y: TYPE.Text (The type of Armor).
-   y: LIST (Checks that the equipped Armor is one the
    character is proficient with).



What it does
------------

Checks for equipped Armor.

Examples
--------

`PREARMORTYPE:1,Chainmail,Full Plate`

Character must have either "Chainmail" or "Full Plate" armor equipped.

`PREARMORTYPE:1,Leather Armor%`

The "%" allows for items named Leather Armor (Masterwork), Leather Armor
(+1) etc.

`PREARMORTYPE:1,TYPE.Medium`

Character must have a Medium type armor equipped.

`PREARMORTYPE:1,LIST`

Character must be proficient in the armor equipped.

