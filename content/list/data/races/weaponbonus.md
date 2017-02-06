+++
date = "2016-08-01"
title = "WEAPONBONUS (Data: races.lst)"
original_url = "/list/data/races.html#weaponbonus"
categories = [ "all-tag", "races-tag" ]
[menu.main]
    name = "WEAPONBONUS (Data: races.lst)"
    parent = "races"
+++

## Status

None

## Syntax

`WEAPONBONUS:x|x`

## Parameters

-   x: Text (Weapon Name)
-   x: TYPE.Text (Weapon Type)



**<span id="weaponbonus"></span> \*\*\* Updated 5.7.12**

What it does
------------

This is a | (pipe) delimited list of weapons or weapon types that are
granted to the race as a choice of ONE of the listed weapons.

Example
-------

`WEAPONBONUS:Rapier|Longbow`

The race receives bonus proficiency in "Rapier" or "Longbow".

`WEAPONBONUS:TYPE.Simple`

The race receives bonus proficiency in any one Simple weapon.

**.MOD Example:**

Initial Race: `Grunt <tab> WEAPONBONUS:TYPE.Simple`

Modified By: `Grunt.MOD <tab> WEAPONBONUS:TYPE.Martial`

Is Equivalent To: `Grunt <tab> WEAPONBONUS:TYPE.Simple|TYPE.Martial` .

The Grunt may choose between Simple and Martial weapons for a single
bonus weapon proficiency.

