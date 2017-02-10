+++
date = "2016-08-01"
title = "PREPROFWITHARMOR (Global: PRErequisite)"
original_url = "/list/global/pre.html#preprofwitharmor"
categories = [ "all-tag", "pre-tag" ]
[menu.main]
    name = "PREPROFWITHARMOR"
    parent = "global_pre"
+++

## Status

New 5.15.8

## Syntax

`PREPROFWITHARMOR:x,y,y`

## Parameters

-   x: Number (The number of armor
    proficiencies needed).
-   y: Text (The name of a Armor Prof).
-   y: TYPE.Text (The type of Armor prof).



What it does
------------

Checks for Armor proficiency requirements.

Examples
--------

`PREPROFWITHARMOR:1,Chainmail,Full Plate`

Character must be proficient with either "Chainmail" or "Full Plate".

`PREPROFWITHARMOR:1,TYPE.Medium`

Character must be proficient with Medium armor.

