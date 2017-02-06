+++
date = "2016-08-01"
title = "FOLLOWER (Data: companion_mods.lst)"
original_url = "/list/data/companionmodifiers.html#follower"
categories = [ "all-tag", "companionmodifiers-tag" ]
[menu.main]
    name = "FOLLOWER (Data: companion_mods.lst)"
    parent = "companionmodifiers"
+++

## Status

None

## Syntax

`FOLLOWER:x,x=y`

## Parameters

-   x: Text (Class name or Variable)
-   y: Number (Class level or Variable value)



What it does
------------

-   This is a comma delimited list of classes or variables.
-   If the "master" meets the required level or value in the tag, then
    the companion gains all the benefits as described by the other tags
    in the line.

Examples
--------

`FOLLOWER:Paladin=5`

True if PC is a Level 5 or greater "Paladin".

`FOLLOWER:Sorcerer,Wizard=1`

True if PC is a Level 1 or greater "Sorcerer" or "Wizard".

`FOLLOWER:CompanionLevel=5`

True if the CompanionLevel variable is 5 or greater.

