+++
date = "2016-08-01"
title = "WEAPONBONUS (Data: templates.lst)"
original_url = "list/data/templates.html#weaponbonus"
categories = [ "all-tag", "templates-tag" ]
+++

## Status

Updated 5.7.12

## Syntax

`WEAPONBONUS:x|x`

## Parameters

-   x: Text (Weapon Name)
-   x: TYPE.Text (Weapon Type)



What it does
------------

-   This is a pipe-delimited (|) list of weapons or weapon types that
    are granted to the race as a choice of ONE of the listed weapons.
-   **.MOD Behavior:** When modifying a template, with the `.MOD` tag,
    given an existing `WEAPONBONUS` tag, the data included in a new
    `WEAPONBONUS` tag will be appended to the existing tag data.

Example
-------

`WEAPONBONUS:Rapier|Longbow`

The race receives bonus proficiency in "Rapier" or "Longbow".

`WEAPONBONUS:TYPE.Simple`

The race receives bonus proficiency in any one Simple weapon.

**.MOD Example:**

Initial Template: `Grunt <tab> WEAPONBONUS:TYPE.Simple`

Modified By: `Grunt.MOD <tab> WEAPONBONUS:TYPE.Martial`

Is Equivalent To: `Grunt <tab> WEAPONBONUS:TYPE.Simple|TYPE.Martial` .

The Grunt may choose between Simple and Martial weapons for a single
bonus weapon proficiency.

